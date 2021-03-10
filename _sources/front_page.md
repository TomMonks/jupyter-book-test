# Getting started with Jupyter Books

## Method overview

1. Set up repository (repo) on GitHub (github.com)
1. Clone repo to local computer
1. Create a folder for book content (markdown pages and Jupyter notebooks)
1. Add required content
1. Create a table of contents _toc.yml file in content folder
1. Build book
1. Use `ghp-import` to push contents of book to GitHub (creates a `gh-pages` branch)
1. Go to GitHub repo settings, and activate GitHub pages (point to `gh-pages`) and copy link to webiste

## Table of contents

The order, and breakdown, of the book is held in the `_toc.yml` file in the book contents. folder.

This file may be as simple as a list of required markdown and notebook pages with the syntax `- file filename_with_no_extension`.

The `_toc.yml` may also be used to add structure such as parts, chapters and sections.

For example this book uses the following in the _toc.yml file:

'''

'''


## Building the book

Install Jupyter Book with `pip install jupyter-book`. This will need to be done in each environment where you are using Jupyter Book.

Build book with the `jupyter-book build` command followed by the contents directory, e.g. `jupyter-book build ./content` 

This will create a `_build` folder that contains html. You can check the pages work by opening them on your computer.

## Pushing to GitHub

First install ghp-import with `pip install ghp-import`. This will need to be done in each environment where you are using Jupyter Book.

Then go to the folder which contains the `_build` folder, and from a terminal run:

`ghp-import -n -p -f _build/html`

This pushes the htmp up to the GitHub repo, into a branch called `gh-pages` (which it creates if necessary).

## Activating the pages

In the GitHub repo, go to settings and scroll down to GitHub pages. Select the `gh-pages` as the source. This is all you need to do. It provides the link for the home page when you do this.

## Config file

You may also specify a _config.yml file. This may be used to refine the notebook, for example giving a title, or specifying whether to use cached notebook content (or re-run notebooks).

See the example in the GitHub repo.

