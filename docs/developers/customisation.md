# SDGRP - Customisation

Prior to getting started with customising the platform, you should have already forked a "starter" repository, and renamed it to something like `sdg-indicators-sweden` (for example). If you have not done this yet, [start here](forking.md). In this documentation we will refer to this as the "site repository".

## Jekyll configuration

Jekyll configuration is stored at the root of the site repository in a YAML file called `_config.yml`. General documentation about Jekyll configuration can be found [here](https://jekyllrb.com/docs/configuration/).

Additionally, here are some commonly-used configuration items specific to this platform, along with examples in the YAML format:

```
# This tells the platform's Javascript code where pull remote data from.
remotedatabaseurl: "https://my-github-organisation.github.io/sdg-data-sweden"

# This tells Jekyll itself where to pull remote data from.
jekyll_get_data:
  # Pull in the metadata for all the indicators.
  - data: meta
    json: 'https://my-github-organisation.github.io/sdg-data-sweden/meta/all.json'
  # Pull in the headlines for all the indicators.
  - data: headlines
    json: 'https://my-github-organisation.github.io/sdg-data-sweden/headline/all.json'
  # Pull in the metadata schema for the indicators.
  - data: schema
    json: 'https://my-github-organisation.github.io/sdg-data-sweden/meta/schema.json'
  # Pull in the text translations for SDG-related words/phrases.
  - data: translations
    json: 'https://opendataenterprise.github.io/sdg-translations/translations.json'

# Set the email addresses that appear on the platform
email_contacts:
  questions: questions@example.com
  suggestions: suggestions@example.com
  functional: functional@example.com

# For Prose.io integration, some information about the "data repository".
repo_name: sdg-data-sweden
branch: develop
org_name: my-github-organisation

# Some information about your locale.
country:
  name: Sweden
  adjective: Swedish

# Control the items in the main menu.
menu:
  - path: /reporting-status
    translation_key: reporting_status
  - path: /about
    translation_key: about
  - path: /guidance
    translation_key: guidance
  - path: /faq
    translation_key: faq

# The list of languages that are translated. The first one is the default.
languages:
  - en
  - es
  - fr

# Tell Jekyll to use the Remote Theme plugin.
plugins:
  - jekyll-remote-theme

# Tell the Remote Theme plugin to use this project!
remote_theme: ONSDigital/sdg-reporting

# Load any number of custom CSS files.
custom_css:
  - /assets/css/custom.css
```

## Working with (remote) Jekyll themes


