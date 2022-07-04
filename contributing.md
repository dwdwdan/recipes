---
title: Contributing
---
# Contributing

To contribute, please submit a pull request to [this github repo](https://github.com/dwdwdan/recipes)
or email me at [dwdwdan@gmail.com](mailto:dwdwdan@gmail.com).

Contribution must be added to the `_posts` folder with the name `YYYY-MM-DD-Post-Title.md`, replacing the post title with
an appropriate name for your recipe.

The file has to start with the frontmatter

```
---
title: Recipe Name
author: Author Name
shortDesc: A short description of the recipe. This can be written in markdown but try to keep it to a minimum
serves: number that the recipe serves
---
```

After this you have freedom to use markdown however you wish, but you should try to follow a similar style to the posts
already in the `_posts` folder.

## Recipe Guidelines

The general form should be something similar to
```
## Ingredients
- Ingredient 1
- Ingredient 2

## Method
1. Step 1
2. Step 2
3. Step 3

Adapted from [source_name](source_link)
```
with the last line of course being optional.
The short description from the frontmatter will be automatically displayed below the recipe's title along with the author and date.

## Checking the generated output
It is not necessary for you to check the recipe looks good in the website (I will always do this before authorising a PR anyway), but if you want to, here are some instructions:

First, you will need to have ruby and rubygems installed (see [rubygems.org](rubygems.org)). For me, on fedora linux, this can be done with
```
$ sudo dnf install ruby rubygems
```
Then, use the gem package manager to install bundler
```
$ sudo gem install bundler
```
There is a config file for bundler included in this repository, so then you should be able to run
```
$ bundle install
```
to install all dependencies.

Finally, you can tell jekyll to serve the website using
```
$ bundle exec jekyll serve
```
this will give you a web address that the website is being served at, probably beginning with `localhost`. If you additionally include the `-l` flag to the `bundle exec` command, your browser will automatically reload when you make changes to the files.
