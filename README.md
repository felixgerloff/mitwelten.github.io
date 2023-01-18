# Mitwelten Web Static
Hugo source code of the static part, to be hosted on www.mitwelten.org.

Hosting is not yet automated, you'll have to preview on your Mac.

Publishing requires copying files to [mitwelten.github.io](https://github.com/mitwelten/mitwelten.github.io).

## Install Hugo
On your Mac, open a Terminal and type

```
$ brew install hugo
$ hugo version
```

## Get this repo
To clone the repo with git, type

```
$ cd ~/Desktop # (or wherever you like)
$ git clone https://github.com/mitwelten/mitwelten-web-static
$ cd mitwelten-web-static
```

## Run a local server
To run a local Web server, type

```
$ cd ~/Desktop/mitwelten-web-static
$ hugo server -D
(visit http://localhost:1313/)
```

## Set up to publish
To set up publishing to www.mitwelten.org, type

```
$ cd ~/Desktop # (or wherever you keep mitwelten-web-static)
$ git clone https://github.com/mitwelten/mitwelten.github.io
$ npm install autoprefixer
```

## Publish to mitwelten.org
To publish to www.mitwelten.org (assuming you're [set up to publish](#set-up-to-publish)), type

```
$ cd ~/Desktop/mitwelten-web-static
$ git pull
$ hugo
$ cp -r public/ ../mitwelten.github.io
$ cd ../mitwelten.github.io
$ git status # check changed files
$ git commit --all
$ git push
(visit https://www.mitwelten.org/)
```

## Add a post
To add a new post, type

```
$ cd ~/Desktop/mitwelten-web-static
$ hugo new posts/my-new-post.md
$ open content/posts/my-new-post.md
(edit, save your new post)
(check http://localhost:1313/posts)
```

## Add a device
To add a new device (i.e. using a custom archetype and custom shortcodes to embed charts, maps), type

```
$ cd ~/Desktop/mitwelten-web-static
$ hugo new id/0000-0004.md
$ open content/id/0000-0004.md
(edit, save your new device)
(check http://localhost:1313/id)
```
> Note: The convention would require `ids`, but we already commited to `id`.

## Check the file structure
```
$ cd ~/Desktop/mitwelten-web-static
$ brew install tree
$ tree
.
├── LICENSE
├── README.md
├── archetypes
│   └── id.md
├── assets
│   └── scss
│       └── _variables_project.scss
├── config.toml
├── content
│   └── de
│       ├── _index.html
│       ├── about
│       │   ├── _index.html
│       │   └── featured-background.jpg
│       ├── blog
│       │   ├── _index.md
│       │   ├── news
│       │   │   ├── _index.md
│       │   │   ├── first-post
│       │   │   │   ├── featured-sunset-get.png
│       │   │   │   └── index.md
│       │   │   └── second-post.md
│       │   └── releases
│       │       ├── _index.md
│       │       └── in-depth-monoliths-detailed-spec.md
│       ├── docs
│       │   ├── Concepts
│       │   │   └── _index.md
│       │   ├── Contribution guidelines
│       │   │   └── _index.md
│       │   ├── Examples
│       │   │   └── _index.md
│       │   ├── Getting started
│       │   │   ├── _index.md
│       │   │   └── example-page.md
│       │   ├── Overview
│       │   │   └── _index.md
│       │   ├── Reference
│       │   │   ├── _index.md
│       │   │   └── parameter-reference.md
│       │   ├── Tasks
│       │   │   ├── Ponycopters
│       │   │   │   ├── _index.md
│       │   │   │   ├── configuring-ponycopters.md
│       │   │   │   └── launching-ponycopters.md
│       │   │   ├── _index.md
│       │   │   ├── beds.md
│       │   │   ├── porridge.md
│       │   │   └── task.md
│       │   ├── Tutorials
│       │   │   ├── _index.md
│       │   │   ├── multi-bear.md
│       │   │   └── tutorial2.md
│       │   └── _index.md
│       ├── featured-background.jpg
│       ├── id
│       │   ├── 0000-0001.md
│       │   ├── 0000-0002.md
│       │   └── 0000-0003.md
│       └── search.md
├── go.mod
├── go.sum
├── layouts
│   ├── 404.html
│   └── shortcodes
│       ├── swisstopo.md
│       └── thingspeak.html
├── netlify.toml
├── package.json
├── resources
│   └── _gen
├── static
│   └── images
│       ├── dreispitz.png
│       ├── merian.png
│       └── reinach.png
└── themes
    └── docsy

```

# Docs
The following links provide technical background.

## Installing & Usage
* https://gohugo.io/getting-started/installing/
* https://gohugo.io/getting-started/usage/

## Templates (based on HTML)
* https://gohugo.io/templates/base/
* https://gohugo.io/templates/homepage/

## Content Management (based on Markdown)
* https://gohugo.io/getting-started/quick-start/
* https://gohugo.io/content-management/archetypes/
* https://gohugo.io/content-management/shortcodes/
