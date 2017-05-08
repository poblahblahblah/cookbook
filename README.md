# O'Brien Family Cookbook
This is the O'Brien Family Cookbook website, which contains some or most of our favorite family recipes. No more do you have to search your email for an email you were sent 8 years ago that is now potentially out of date!

This repo itself is a [middleman](https://middlemanapp.com/) powered blog that has been altered a bit to work as a cookbook. The theme is provided by the [middleman-casper](https://github.com/danielbayerlein/middleman-casper) project.

## Making Changes
### Prerequisites
You will need a modern ruby (I am currently using 2.3.x) and a modern install of rubygems. Once those two requirements are satisfied cd into the cookbook directory and type `bundle` to get all dependencies installed locally.

### Running the web server
Once prerequisites are installed, cd to the repo and type `middleman` to start the web server. You can now browse to http://localhost:4567 to view the site. The only thing that doesn't work is search since the middleman-search gem will need a search index that is not built until deploy time.

### Adding a recipe
All recipes can be found in `source/recipes`. The file name should be `recipe-name.html.markdown` and the recipe should follow this [recipe template](https://gist.githubusercontent.com/anonymous/ff969d248019f2e5b105b3819889ddd2/raw/fb1da5f549890a5418042ef5b2a9af82803ed869/gistfile1.txt). Once you add a file to the directory you should be able to hit refresh in your browser and have the recipe show up in the recipe list.

### Pushing your changes
Once your changes are made you can type in `rake deploy` to have the site built and deployed to S3.
