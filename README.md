# Hugo Starter Kit with Gulp Asset Pipeline and Bulma.io

## About This Kit

This kit includes basic boilerplate for creating static sites with [Hugo](https://gohugo.io/) and basic stylic with [Bulma.io](http://bulma.io/). 

If you are confused about source organization, build steps, modules, etc, every partial, `.js`, and `.scss` file includes thorough comments. 

For more detailed information on the Gulp Asset Pipeline, see the [README in the `assets` folder](https://github.com/Epick362/bulma-hugo-static-starter/tree/master/assets).

## Requirements

* Hugo. [The Hugo site provides installation instructions](https://gohugo.io/overview/installing/).
* Node.js. You can download and install Node via the [Node.js installer page](https://nodejs.org/en/download/). Installation includes NPM, the package manager for Node. You will need both to run the asset pipeline.
* Git. Put your project in version control if you're willing to do more than download the zip. I cannot emphasize this enough.

> **Note:** If this is your first experience with any of the above tools, I'd recommend installing Node.js, Hugo, *and* Git via the [Homebrew Package Manager for OSX](https://github.com/Homebrew/homebrew/tree/master/share/doc/homebrew#readme)

## Getting Started

Once you've installed the requirements - 

* `cd ~/path/to/your/site/directory/`
* `git clone https://github.com/Epick362/bulma-hugo-static-starter`
* `cd bulma-hugo-static-starter && hugo serve`
* (New Terminal Tab) `cd assets/ && npm install` 
* `gulp`
* Open your browser to `localhost:1313`.

## Features

### Gulp Asset Pipeline (See README in `assets/` for details)

* CSS reset
* SASS compiling with minification and autoprefixer 
* `variables.scss` for easier customization
* [Bourbon](http://bourbon.io/) and [Neat](http://neat.bourbon.io/) Mixins 
* JavaScript concatenation, minification, and [ES2015 transpilation](https://babeljs.io/)

### Global Partials

* Create your pages with `{{ partial "site_header.html" }}` and `{{ partial "site_footer.html" }}` on all single or list layouts 
* `site_header.html` includes the following:
    * Metadata:
        * Favicons
        * [OGP](http://ogp.me/) for social sharing
        * [Swiftype V2 Metadata](https://swiftype.com/documentation/meta_tags2). This can be removed if you do not intend to use Swiftype.
    * Site stylesheet
        * Via `<link rel="stylesheet">` OR direct embed for critical render path. See comment in `config.toml` for more directions
    * Site `<header>`:
        * global navigation
        * search form
* `site_footer.html` includes the following:  
    * Copyright Line 
    * Footer navigation
    * Site scripts with conditional templating to add page- or section-specific scripts
    * Social media list with SVG icons

### `/content/singletons/` Section with `singletons-stylesheets` and `alt-scripts`

* `/content/singletons/` allows for singleton pages requiring alternative stylesheets and scripts
* `temp` creates one-off pages with convenient short URLs (see `[permalinks]` in `config.toml`)

## `config.toml`

* Sane site parameters pulled from Hugo docs example
* Disqus comments 
* Social media
* Taxonomies (tags, categories)
* jQuery CDN (boolean)
* Minimal BlackFriday settings
   
   
## Original project without Bulma.io dependency can be found here: https://github.com/rdwatters/hugo-starter
