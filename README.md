# cardano-learn
Learning about Cardano


## Setup

See [prerequisites](https://foo-dogsquared.github.io/blog/posts/blogging-with-asciidoctor-and-hugo/#_prerequisites)

Install Hugo: https://gohugo.io/getting-started/installing/#binary-cross-platform

Windows
Install hugo and ruby from an elevated command prompt

```console
choco install hugo --confirm
choco install ruby
```
Now install ascidoctor using ruby's gem from a new command prompt. More info [here](https://docs.asciidoctor.org/asciidoctor/latest/install/ruby-packaging/).

```
# install asciidoctor
gem install asciidoctor
```

## Quick Start

```
hugo new site cardano-learn-site
cd site cardano-learn-site
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
```

Append the line `theme = 'ananke'` at the end of config.toml file

### Create some content

```
hugo new posts/my-first-post.md
```

Edit the post in `content/posts/my-first-post.md' by adding your content just below the automatically created medatata.
Note: Drafts do not get deployed; once the post is finished, update the header of the post to say draft: false.

```
---
title: "My First Post"
date: 2021-12-08T00:49:35+01:00
draft: false
---

# My First Post with Hugo

Hugo is a nice tool and this is my first post
```

### Start the Local Hugo server 

```
hugo server -D
``` 

Navigate to your new site at http://localhost:1313/

You can edit oradd new content and simply refresh in browser to see changes quickly. 
(You might need to force refresh your web browser, something like Ctrl-R usually works.)

## Hugo + Asciidoc

- 