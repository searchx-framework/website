
## Quick Install

In the case you're installing to existing Jekyll project, add this line to your project's `Gemfile`:

```
gem "jekflix"
```

Add this line to your project's `_config.yml`:

```
theme: jekflix
```

And then run:

```
$ bundle
```

Or install it yourself as:

```
$ gem install jekflix
```

### Theme Colors

Create the file `/assets/css/styles.scss` and add:

```
---
---

$themeColor: #ff0a16;
$primaryDark: #141414;
$accentDark: #ffffff;
$lightGray: #f2f2f2;
$texts: #333333;

@import "jekflix";
```

Modify the variables above to change your theme colors.

### Site configuration

Below are some properties you can change in your project `_config.yml`, check the [documentation](https://github.com/thiagorossener/jekflix-template/wiki/settings) for more details.

```
# Site Settings
name: Jekflix
title: Jekflix | A blog theme for Jekyll
description: Jekflix is a template for Jekyll inspired by Netflix and made by Thiago Rossener.
tags:
  - blog
  - template
  - jekyll
  - theme
  - netlify
email: youremail@xyz.com
disqus_username: disqus_username
show_hero: true
menu:
  - title: Home
    url: /
  - title: About
    url: /about
  - title: Contact
    url: /contact
  - title: Feed
    url: /feed.xml

# Social Media Settings
# Remove the item if you don't need it
github_username: github_username
facebook_username: facebook_username
twitter_username: twitter_username
instagram_username: instagram_username
linkedin_username: linkedin_username
medium_username: medium_username

# Posts Settings
show_time_bar: true
show_modal_on_exit: false
show_modal_on_finish_post: true
two_columns_layout: true

# Advanced Settings
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site
google_analytics: "UA-XXXXXXXX-X"
language: "en"
categories_folder: category
sent_message_url: "/contact/message-sent/"

# Build settings
markdown: kramdown
highlighter: rouge
permalink: /:title/
collections:
  authors:
    output: true
paginate_path: "/page/:num/"
show_get_theme_btn: true
use_logo: false

# Content paginator
paginate_content:
  enabled: true
  debug: false
  collections:
    - posts
  auto: false
  separator: "--page-break--"
  permalink: "/:num/"
  seo_canonical: true
  properties:
    part:
      is_generated: true
    last:
      is_generated: true
    single:
      is_generated: true

# SASS
sass:
  style: compressed

# Plugins
plugins:
  - jekyll-paginate
  - jekyll-paginate-content
```

## Setup

In the case you're cloning this repo, follow those instructions:

- [Environment](https://github.com/thiagorossener/jekflix-template/wiki/setup#environment)
- [Installing template](https://github.com/thiagorossener/jekflix-template/wiki/setup#installing-template)
- [Running local](https://github.com/thiagorossener/jekflix-template/wiki/setup#running-local)

### Customization

See the [settings documentation](https://github.com/thiagorossener/jekflix-template/wiki/settings) to customize layout, titles, social media and more.

### Theme

You can easily change the theme colors by changing the file `src/yml/theme.yml`, then running `gulp build` in your terminal.

#### GitHub pages

It's a known issue that you can't run Gulp when deploying the website into GitHub pages. So, you must change the theme colors and run `gulp build` locally, then push the changes into your repo, there is no other way.

To see how your website is going to look like when you deploy it, run `bundle exec jekyll serve` locally and access `http://127.0.0.1:4000/`.

## Posts

Use the [Front Matter properties](https://github.com/thiagorossener/jekflix-template/wiki/post#front-matter-properties) to create posts.

> **Note:** In the case you're cloning this repo, you can use the available [script](https://github.com/thiagorossener/jekflix-template/wiki/post#creating-a-post) to generate posts automatically.

## Release notes

### v3.1.0

- Fixed hero URL, thanks to [@JoelSalzesson](https://github.com/JoelSalzesson)
- Updated Google Analytics script, thanks to [@JHLeeeMe](https://github.com/JHLeeeMe)
- Added MathJax library to render math expressions, thanks to [@XieGuochao](https://github.com/XieGuochao)

### v3.0.2

- Added assets folder

### v3.0.1

- Fixed post SVG icons

### v3.0.0

- Created theme `gem`
- Enabled text translations
- Added heading anchor links
- Changed code highlight colors
- Changed from Stylus to SASS

### v2.0.1
- Fixed bugs
- Optimized to support disabled JS

### v2.0.0
- Added optional [sidebar](https://github.com/thiagorossener/jekflix-template/wiki/Features#posts-sidebar)
- Added optional [Featured post](https://github.com/thiagorossener/jekflix-template/wiki/features#featured-post)
- Added optional ["Before you go" modal](https://github.com/thiagorossener/jekflix-template/wiki/features#before-you-go-modal)
- Added optional [post pagination](https://github.com/thiagorossener/jekflix-template/wiki/features#paginated-posts)
- Added [post recommendation](https://github.com/thiagorossener/jekflix-template/wiki/features#post-recommendation)
- Added meta keywords to improve SEO
- Added JSON-LD to improve SEO
- Changed pagination to be [optional](https://github.com/thiagorossener/jekflix-template/wiki/features#home-page-pagination)
- Improved [Tags page](https://github.com/thiagorossener/jekflix-template/wiki/features#tags-page)
- Cleaned up and improved [Front Matter properties](https://github.com/thiagorossener/jekflix-template/wiki/post#front-matter-properties)
- Set up [Netlify CMS](https://github.com/thiagorossener/jekflix-template/wiki/features#netlify-cms-ready)
- Improved customization settings
- Minor design updates

### v1.0.1
- Fixed bugs
- Upgraded to Gulp 4

### v1.0.0
- Initial release

## Questions?

File a [GitHub issue](https://github.com/thiagorossener/jekflix-template/issues/new) please.

## Donation

Did you like my work? Buy me a beer 😁🍺

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=SAKL66RSDGH48&source=url)

## Author

[Thiago Rossener](https://rossener.com/)

## License

*Jekflix Template* is available under the MIT license. See the [LICENSE](https://github.com/thiagorossener/jekflix-template/blob/master/LICENSE) file for more info.
