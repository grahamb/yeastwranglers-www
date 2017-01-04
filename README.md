# Yeast Wranglers WWW

## install

* install Ruby and Node.js
* clone this repo
* `gem install bundler`
* `bundler install`
* `npm install`

## To get started

```sh
$ gulp
```

And you'll have a new Jekyll site generated for you and displayed in your
browser. Neato. If you want to run it with production settings, just add
`--prod`.

## File formats

### Markdown

[You can see more on markdown here](https://daringfireball.net/projects/markdown/).

Markdown is like HTML, but simplified. This file is written in Markdown.

### YAML

YML or YAML is a way to represent data as objects. __Indentation matters__. Starting something with `- `
indicates you are starting a new object. 

## Usage

### Build for Production

```sh
$ gulp cleanbuildcopy --prod
```

This will create a folder called `dist/` that has a production ready version of the site.

### Deploy

To deploy the site you must add a `aws-credentials.json` file (ask the site admin for it), build the site and run

```sh
$ gulp deploy
```

Your changes are now live. Double neato.

# Content

## Add a page

create a folder for the page name, ie yeastwraglers.com/blog/ create a folder called blog in `src/` folder. Put a file called `index.html` in the folder.
`index.html` will hold all the content for your page. Add the page to the navigation by adding it to `src/_data/nav.yml`. This works the same for
sub folders, add them as children in `src/_data/nav.yml`.

## Adding a blog post

[You can see a full write up on writing posts here](https://jekyllrb.com/docs/posts/)

Blog posts are stored in the `src/posts` folder. To create a new blog post add a file with the filename like `YYYY-MM-DD-POSTTITLE.markdown`.
Posts are written in Markdown and have YAML metadata in their [front matter](https://jekyllrb.com/docs/frontmatter/).
You can look at existing blog posts for examples, but the [front matter](https://jekyllrb.com/docs/frontmatter/) allows you to set the 
title, date, author, category, and excerpt for the post.

## Add a meeting

Meeting are added and re-ordered via the `src/_data/meeting.yml` file.

## Change the main page carousel

Carousel items can be changed in the `src/_data/slides.yml` file.

## Change the sponsors

Sponsors can be changed in the `src/_data/sponsors.yml` file.

# Change the site navigation

Sponsors can be changed in the `src/_data/nav.yml` file.

## FAQ



This site was generated with `generator-jekyllized`, please refer to the [README
on Github](https://github.com/sondr3/generator-jekyllized).

## for SSL issue

If you get `SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed`. 

Run from the root of the site:

```sh
wget http://curl.haxx.se/ca/cacert.pem
```

and run gulp with

```sh
SSL_CERT_FILE=cacert.pem gulp
```
