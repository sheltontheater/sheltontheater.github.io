# Shelton Theater Website

Website for the Shelton Theater in San Francisco.

## Development

### Prerequisites

- Ruby and Jekyll installed ([Jekyll docs](https://jekyllrb.com/docs/installation/))

### Local Development

Install dependencies:

```
bundle install
```

Start the development server:

```
bundle exec jekyll serve
```

Build the site:

```
bundle exec jekyll build
```

## Site Structure

- `_shows/` - Show/artist pages (uses `page` layout with `page-show` body class)
- `_layouts/` - Page templates
- `_includes/` - Reusable components
- `_sass/` - SCSS stylesheets
- `_data/` - Site data (menus, contact info)
- `images/` - Site images

### Adding a New Show

Create a new file in `_shows/` with front matter:

```yaml
---
title: Show Name
permalink: /show-slug/
hero_image: /images/shows/hero.jpg
weight: 1
---

Show description here.
```

### Front Matter Options

The `page` layout supports these front matter options:

```yaml
hero_image: /images/hero.jpg    # Hero image at top of page
hero_alt: Description of image  # Alt text (defaults to page title)
tickets_url: https://...        # Shows "Buy Tickets" button
website_url: https://...        # Shows "Website" button
show_call: true                 # Shows contact info box
gallery:                        # Image gallery
  - src: /images/photo1.jpg
    alt: Description
```

### Hero Images

Recommended image ratio: **3:1** (e.g., 1800x600px).

## Deployment

The site is hosted on [GitHub Pages](https://pages.github.com/). Pushing to the `master` branch automatically triggers a build and deployment.

## Credits

Based on the [Jekyll Serif Theme](https://github.com/zerostaticthemes/jekyll-serif-theme) by [Zerostatic](https://www.zerostatic.io).
