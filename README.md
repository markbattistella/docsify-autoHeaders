<div align="center">

# docsify-autoHeaders

![Github2npm](https://github.com/markbattistella/docsify-autoHeaders/workflows/gh2npm/badge.svg?event=registry_package) ![npm (scoped)](https://img.shields.io/npm/v/@markbattistella/docsify-autoheaders) ![GitHub](https://img.shields.io/github/license/markbattistella/docsify-autoheaders) ![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@markbattistella/docsify-autoheaders)

---

[![](https://img.shields.io/badge/%20-@markbattistella-blue?logo=paypal&style=for-the-badge)](https://www.paypal.me/markbattistella/6AUD)
[![](https://img.shields.io/badge/%20-buymeacoffee-black?logo=buy-me-a-coffee&style=for-the-badge)](https://www.buymeacoffee.com/markbattistella)

[![](https://img.shields.io/badge/demo-@markbattistella/docsify--autoHeaders-1E5749?style=for-the-badge)](https://markbattistella.github.io/docsify-autoHeaders/)

</div>

---

# Auto number headings

This plugin is designed to create heading numbers in your pages if you are creating a reference guide.

It stops you from having to manually number the heading, and then have to then trawl through every heading afterwards to change the numbering system again.

It allows you to either have all the headings in one page, or if you split them over many `markdown` documents then specify what the heading number it should be starting at.

## Installation

### Update `index.html` file

Assuming you have a working [docsify](https://docsify.js.org/) framework set up, it is easy to use the plugin.

1. Add the following script tag to your `index.html` via either CDN or downloading it and using it locally:

    ```html
    <!-- unpkg.com -->
    <script src="https://unpkg.com/@markbattistella/docsify-autoheaders@latest"></script>

    <!-- jsDelivr -->
    <script src="https://cdn.jsdelivr.net/npm/@markbattistella/docsify-autoheaders@latest"></script>

    <!-- locally -->
    <script src="docsify-autoheaders.min.js"></script>
    ```

1. In docsify setup configure the plugin (see [configuration](#configuration) for setup):

    ```js
    <script>
    window.$docsify = {
      autoHeaders: {
        separator: String,  // how numbers should be separated
        levels:    String,  // heading levels h[1-6]
        scope:     String,  // plugin search scope
        debug:     Boolean  // show console.log messages
      },
    };
    </script>
    ```

### npm install

Or if you're using `npm` to manage your dependencies:

```sh
npm i @markbattistella/docsify-autoheaders
```

### Configuration

There are some options available for the `docsify-autoHeaders`:

| setting   | options                                                         |
|-----------|-----------------------------------------------------------------|
| separator | how the numbers are separated - `decimal`, `dash`, or `bracket` |
| levels    | heading levels to target `1-6`                                  |
| scope     | the element to narrow it down to. `#main` is the default scope  |
| debug     | `true` or `false` if you want to see `console.log` info         |

### Usage

At the top of your file add the following snippet:

```md
@autoHeader:#
```

At the end of the identifier `(marked with #)`, add the starting heading number. If you don't have a valid entry then it won't auto number.

It accepts only numbers, and decimals are rounded down.

You can have a starting header at `0` using:

```md
@autoHeader:0
```

## Roadmap

Looking ahead, I want to add in the ability to start all levels of headings:

```md
@autoheaders:3.5.6.6.1.12

##### New heading
```

Respectively starting the first heading at:

    3.5.6.6.2.1 New heading

## Contributing

1. Clone the repo:

    `git clone https://github.com/markbattistella/docsify-autoHeaders.git`

1. Create your feature branch:

    `git checkout -b my-feature`

1. Commit your changes:

    `git commit -am 'Add some feature'`

1. `Push` to the branch:

    `git push origin my-new-feature`

1. Submit the `pull` request
