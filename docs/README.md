# Sustainable Development Goals - Reporting Platform

## Overview

This is the centerpiece of several repositories comprising a reporting platform for the [Sustainable Development Goals](https://www.un.org/sustainabledevelopment/sustainable-development-goals/) (SDG). In addition to displaying SDG indicator data to the general public, this platform serves as a data management system. It is built with open-source libraries and tools, and can be hosted and maintained with free services.

## Quick start

This platform is designed to be implemented quickly, easily, and free of cost. To try it out for yourself, visit the [quick start](developers/quick-start) section.

## Policy makers

Visit the [policy makers](policy-makers/overview) section for answers to these questions:
* What is a National Reporting Platform (NRP)?
* Can this platform be used as a Local Reporting Platform (LRP)?
* Why chose an NRP or LRP?
* What does this platform cost?
* Who else is using this platform?

## Data providers

Visit the [data providers](data-providers/overview) section for answers to these questions:
* What is the best way to identify data gaps?
* How can I update data and metadata?
* How can I review changes to data and metadata?
* In what format will the data and metadata be stored?
* In what formats will the data and metadata be available to the public?

## Developers

Visit the [developers](developers/overview) section for answers to these questions:
* What are the IT requirements for this platform?
* How do I install this platform?
* How can this platform be customised?
* What are the options for deploying this platform?
* How can I translate this platform into other languages?






## Usage

The recommended way to use this theme is through the [jekyll-remote-theme](https://github.com/benbalter/jekyll-remote-theme) plugin. This can be done by adding the following code to your site's `_config.yml` file:

```
plugins:
  - jekyll-remote-theme
remote_theme: ONSDigital/sdg-theme
```

## Translation data

This theme relies on translation data being pulled in from the [sdg-translations](https://github.com/brockfanning/sdg-translations) repository, at build time. This can be accomplished by using the [jekyll-get](https://github.com/18F/jekyll-get) plugin and this `_config.yml` code:

```
jekyll_get:
  - data: translations
    json: 'http://brock.tips/sdg-translations/translations.json'
```

## Customising

Like any [Jekyll theme](https://jekyllrb.com/docs/themes/), `sdg_theme` can be customised by overriding markup and assets. You can override any file in the `_includes`, `_layouts`, and `assets` folders, by placing an identically-named file in the corresponding folder of your site repository. Eg, to override the `_includes/components/breadcrumb.html` file in this theme, place a file at `_includes/components/breadcrumb.html` in your site repository, and customise to your liking.

For simple text changes, however, it may be easier to override the translation data mentioned above.
