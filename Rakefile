deploy_default = "s3"
s3_bucket       = "obrieneats.com"
aws_cli_path    = "/usr/local/bin/aws"
aws_region      = "us-west-1"

desc "Build the website from source"
task :build do
  puts "## Building website"
  status = system("middleman build --clean")
  puts status ? "OK" : "FAILED"
end

desc "Deploy website via aws s3 sync"
task :s3 do
  puts "## Deploying website via aws s3 sync"
  system("#{aws_cli_path} s3 sync build/ s3://#{s3_bucket}/ --region #{aws_region} --profile madelinefox")
end

desc "Deploy files to S3"
task :deploy => [:build, :s3]
task :default => :deploy

