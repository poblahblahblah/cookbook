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

desc "Deploy website via middleman-deploy to gh-pages branch"
task :deploy_pages do
  puts "## Deploying website to gh-pages"
  system("middleman deploy")
end

task :deploy => [:build, :deploy_pages]
task :default => :deploy

