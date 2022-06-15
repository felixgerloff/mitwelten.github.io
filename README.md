# Mitwelten Web Static Proof of Concept
Here's a minimal site (no theme, no CSS)  to show the different concepts.

Hosting is not yet solved, you'll have to try it on your Mac.

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
$ git clone https://github.com/mitwelten/mitwelten-web-static-poc
$ cd mitwelten-web-static-poc
```

## Run a local server
To run a local Web server, type

```
$ cd ~/Desktop/mitwelten-web-static-poc
$ hugo server -D
(visit http://localhost:1313/)
```

## Add a post
To add a new post, type

```
$ cd ~/Desktop/mitwelten-web-static-poc
$ hugo new posts/my-new-post.md
$ open content/posts/my-new-post.md
(edit, save your new post)
(check http://localhost:1313/posts)
```

## Add a device
To add a new device (i.e. using a custom archetype and custom shortcodes to embed charts, maps), type

```
$ cd ~/Desktop/mitwelten-web-static-poc
$ hugo new id/0000-0004.md
$ open content/id/0000-0004.md
(edit, save your new device)
(check http://localhost:1313/id)
```
> Note: The convention would require `ids`, but we already commited to `id`.

## Check the file structure
```
$ cd ~/Desktop/mitwelten-web-static-poc
$ brew install tree
$ tree
.
├── LICENSE
├── README.md
├── archetypes
│   ├── default.md
│   └── id.md
├── config.toml
├── content
│   ├── _index.md
│   ├── id
│   │   ├── 0000-0001.md
│   │   ├── 0000-0002.md
│   │   └── 0000-0003.md
│   └── posts
│       ├── my-first-post.md
│       └── my-second-post.md
├── layouts
│   ├── _default
│   │   ├── baseof.html
│   │   ├── list.html
│   │   └── single.html
│   ├── index.html
│   └── shortcodes
│       ├── swisstopo.html
│       └── thingspeak.html
├── resources
│   └── _gen
├── static
│   └── images
│       ├── klybeck.png
│       ├── merian.png
│       └── reinach.png
```

This entire part is not relevant right now.

```
└── themes
    └── my-theme
        ├── LICENSE
        ├── archetypes
        │   └── default.md
        ├── layouts
        │   ├── 404.html
        │   ├── _default
        │   │   ├── baseof.html
        │   │   ├── list.html
        │   │   └── single.html
        │   ├── index.html
        │   └── partials
        │       ├── footer.html
        │       ├── head.html
        │       └── header.html
        └── theme.toml
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
