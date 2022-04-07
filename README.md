# terminal-cookbook

![terminal-cookbook](https://github.com/rullmann/hugo-theme-terminal-cookbook/raw/main/images/screenshot.png)

## General information

Thanks to [hugo-cookbook](https://github.com/deranjer/hugo-cookbook) and [recipe-book](https://github.com/rametta/recipe-book). Both inspired this theme and showed that a recipe book is possible with hugo.

The pizza favicon and the boiled egg from the example recipe are provided by [tabler-icons](https://github.com/tabler/tabler-icons) un der the MIT license.

---

## Table of Contents

- [Features](#features)
- [How to start](#how-to-start)
- [How to configure](#how-to-configure)
- [How to write a recipe](#how-to-write-a-recipe)
- [More](#more-things)
  - [featured_image](#featured_image)
  - [Tables](#tables)
- [Known issues](#known-issues)
- [How to edit the theme](#how-to-edit-the-theme)
- [Changelog](CHANGELOG.md)
- [Adjust the style](#adjust-the-style)
- [Licence](#licence)

---

## Features

- Code highlighting thanks to [**HighlightJS**](https://highlightjs.org/) which is build in [**TerminalCSS**](https://terminalcss.xyz) on which this theme relies
- Easy modification to light mode and other fonts after forking this theme
- Tag support for your recipes
- No tracking and analytics code
- No dependency on third-party servers - CSS and JS are part of this repo

## How to start

You can simply add this theme as submodule to your existing or new hugo site:

``` bash
git submodule add https://github.com/rullmann/hugo-theme-terminal-cookbook.git themes/terminal-cookbook
```

## How to configure

This theme is rather simple and requires only a minimal config file. You can copy this example config file and adjust to your hugo site:

``` toml
baseURL = "https://your.subdomain"
languageCode = "en-us"
title = "terminal-cookbook"
theme = "terminal-cookbook"

# optional, if you want to use plain html
# in your markdown recipe files
[markup]
  defaultMarkdownHandler = 'goldmark'
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true
```

## How to write a recipe

- Add your recipes inside a folder `content/recipes` inside your hugo site folder.

Example of markdown metadata:

``` markdown
---
title: "boiled eggs"
summary: "Fantastic boiled eggs - My great-grandpas recipe"
date: 2022-03-23T20:56:42+02:00
draft: false
time: "15m" # how much time it will take to cook this recipe
tags: ["vegetarian", "simple", "one-pot"]
# optional
featured_image: "/boiled-eggs.jpg"
---
## Ingredients

- eggs, as many as you'd like
- water

## Method

1. Put water in pot
2. Boil water
3. Put eggs inside the water
4. Wait 5-8 minutes
```

## More things

### featured_image

You can add photos of your recipes within the `static` folder of your hugo site, e.g. a file `boiled-eggs.jpg` for your recipe above. If the `featured_image` variable is not available no image will be shown.

It's recommended to downscale the images you use here. A height of 1024px should be sufficient for most displays. 

### Tables

If you'd like to use tables inside your reciped (e.g. for your ingredients) just copy and paste this example and adjust to your liking:

```
  <table>
      <thead>
          <tr>
              <!-- table header -->
              <th>amount</th>
              <th>ingredient</th>
          </tr>
      </thead>
      <tbody>
          <tr>
              <th>4</th>
              <td>eggs, raw</td>
          </tr>
          <tr>
              <th>1 litre</th>
              <td>water</td>
          </tr>
      </tbody>
  </table>
```

## Known issues

None right now. You can open an issue (or a pull request) if you find one.

## How to edit the theme

You can fork this repo do whatever you want (see LICENSE for details).

### Adjust the style

This theme is based on [**TerminalCSS**](https://terminalcss.xyz/). If you want to use a light theme you can edit the file `layouts/partials/head.html` and copy the `root` style from the TerminalCSS websites source code.

## Licence

The theme is released under the MIT License. Check the [theme license](/LICENSE) for additional licensing information.
