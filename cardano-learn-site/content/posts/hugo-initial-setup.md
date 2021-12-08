---
title: "Hugo Initial Setup"
date: 2021-12-08T00:56:38+01:00
draft: false
---

# Hugo Initial Setup

Here is a quickstart on how to quickly setup and test a Hugo website on Windows.

## Install

Install hugo from an elevated command prompt

```console
choco install hugo --confirm
```

## Quick Start

Generate a new site

```
hugo new site cardano-learn-site
cd cardano-learn-site
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
git commit -m "Added the submodule themes/ananke"
```

Append the line `theme = 'ananke'` at the end of config.toml file

Note: if you want to push your changes to git repo later, don't forget to execute `git commit -m "Added the submodule themes/ananke"` for adding the submodule to the repository.

### Create some content

```
hugo new posts/my-first-post.md
```

Edit the post in `content/posts/my-first-post.md` by adding your content just below the automatically created medatata.
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

Navigate to your new site at [http://localhost:1313](http://localhost:1313/)

You can edit or add new content and simply refresh in browser to see changes quickly. Just don't forget to set `draft: false` for new content.
(You might need to force refresh your web browser, something like Ctrl-R usually works.)

### Deploy on GitHub


For more info, read the [Host on GitHub](https://gohugo.io/hosting-and-deployment/hosting-on-github/) document. 

In this example, I will publish a project site, that means it is connected to this specific project on GitHub.
*Note*: GitHub Pages sites are publicly available on the internet by default, even if the repository for the site is private or internal.

