Hyde-X
======

Enhanced port of the Jekyll "[Hyde](https://github.com/poole/hyde)" theme to the [Hugo](http://gohugo.io) site generator. Check below for a list of enhancements.

You can find a live site using this theme [here](http://andreimihu.com) and the corresponding source code [here](https://github.com/zyro/andreimihu.com).

* [Installation](#installation)
* [Usage](#usage)
* [Configuration](#configuration)
* [Built-in colour themes](#built-in-colour-themes)
* [Tips](#tips)
* [Changes and enhancements from the original theme](#changes-and-enhancements-from-the-original-theme)
* [Attribution](#attribution)
* [Questions, ideas, bugs, pull requests?](#questions-ideas-bugs-pull-requests)
* [License](#license)

### Installation

```
$ cd your_site_repo/
$ mkdir themes
$ cd themes
$ git clone https://github.com/zyro/hyde-x
```

See the [official Hugo themes documentation](http://gohugo.io/themes/installing) for more info.

### Usage

This theme expects a relatively standard Hugo blog/personal site layout:
```
.
└── content
    ├── post
    |   ├── post1.md
    |   └── post2.md
    ├── license.md        // this is used in the sidebar footer link
    └── other_page.md
```

Just run `hugo --theme=hyde-x` to generate your site!

### Configuration

An example of what your site's `config.toml` could look like. All theme-specific parameters are under `[params]` and standard Hugo parameters are used where possible.

``` toml
baseurl = "http://example.com/"
title = "Your site title"
languageCode = "en-us"
disqusShortname = "your_disqus_shortname" # Optional, enable Disqus integration
MetaDataFormat = "toml"
theme = "hyde-x"
paginate = 10

[author]
    name = "Your Name"

[permalinks]
    # Optional. Change the permalink format for the 'post' content type.
    # The format shown here is the same one Jekyll/Octopress uses by default.
    post = "/blog/:year/:month/:day/:title/"

[taxonomies]
    # Optional. Use if you want tags and lists.
    category = "categories"

#
# All parameters below here are optional and can be mixed and matched.
#
[params]
    # If false display full article contents in blog index.
    # Otherwise show description and 'read on' link to individual blog post page.
    # Default (if omitted) is true.
    truncate = true

    # Used when a given page doesn't set its own.
    defaultDescription = "Your default page description"
    defaultKeywords = "your,default,page,keywords"

    # Hide estimated reading time for posts.
    # Default (if omitted) is false.
    hideReadingTime = false

    # Changes sidebar background and link/accent colours.
    # See below for more colour options.
    # This also works: "theme-base-08 layout-reverse", or just "layout-reverse".
    theme = "theme-base-08"

    # Select a syntax highight.
    # Check the static/css/highlight directory for options.
    highlight = "sunburst"

    # Optional additional custom CSS file URL, will override other styles.
    customCSS = ""

    # Displays under the author name in the sidebar, keep it short.
    # You can use markdown here.
    tagline = "Your favourite quote or soundbite."

    # Text for the top menu link, which goes the root URL for the site.
    # Default (if omitted) is "Blog".
    home = "Blog"

    # Metadata used to drive integrations.
    googleAnalytics = "Your Google Analytics tracking code"
    gravatarHash = "MD5 hash of your Gravatar email address"

    # Sidebar social links, these must be full URLs.
    github = ""
    bitbucket = ""
    stackOverflow = ""
    linkedin = ""
    googleplus = ""
    facebook = ""
    twitter = ""
    youtube = ""

    # Other social-like sidebar links
    rss = false  # switch to true to enable RSS icon link
    flattr = ""  # populate with your flattr uid
```

### Built-in colour themes

Hyde-X provides 8 built-in colour themes by default, with the option to define more in your own custom CSS.

![Hyde-X theme classes](https://github.com/zyro/hyde-x/blob/master/images/theme-colours.png)

### Tips

* If you've added `theme = "hyde-x"` to your `config.toml`, you don't need to keep using the `--theme=hyde-x` flag!
* Pages where you specify `menu = "main"` in the front matter will be linked in the sidebar just below the `Blog` link.
* Use the exact permalink format above to maintain old links if migrating from Jekyll/Octopress.
* Although all of the syntax highlight CSS files under the theme's `static/css/highlight` are bundled with the site, only the one you choose will be included in the page and delivered to the browser.
* Change the favicon by providing your own as `static/favicon.png` in your site directory.
* Hugo makes it easy to override theme layout and behaviour, read about it [here](http://gohugo.io/themes/customizing).
* Pagination is set to 10 items by default, change it by updating `paginate = 10` in your `config.toml`.
* Set `truncate = false` in the `[params]` section of your `config.toml` to display full blog post contents in the index page, like the [base Hyde theme](https://github.com/poole/hyde) did.

### Changes and enhancements from the original theme

* Category labels and lists.
* Client-side syntax highlighting through [highlight.js](https://highlightjs.org/), sane fallback if disabled or no JS - infinitely more flexible than the standard Hugo highlighting.
* Disqus integration: comment counts listed under blog entry names in post list, comments displayed at the bottom of each post.
* Gravatar image in sidebar.
* Google Analytics integration.
* Sidebar link layout and footer format changes.
* Blog post list now contains only the post description, not the full contents.
* Paginated blog listing.
* [FontAwesome](http://fortawesome.github.io/Font-Awesome) social links.
* ...many other small layout tweaks!

### Attribution

Obviously largely a port of the awesome [Hyde](https://github.com/poole/hyde) theme.

### Questions, ideas, bugs, pull requests?

All feedback is welcome! Head over to the [issue tracker](https://github.com/zyro/hyde-x/issues).

### License

Open sourced under the [MIT license](https://github.com/zyro/hyde-x/blob/master/LICENSE).
