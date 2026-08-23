[![Varbase](https://raw.githubusercontent.com/Vardot/varbase/11.0.x/images/varbase-logo.png)](https://www.drupal.org/project/varbase)

# Varbase Internationalization Base
[![pipeline status](https://git.drupalcode.org/project/varbase_i18n_base/badges/1.0.x/pipeline.svg)](https://git.drupalcode.org/project/varbase_i18n_base/-/pipelines)
[![Varbase Internationalization Base](https://img.shields.io/badge/Varbase%20Internationalization%20Base-1.0.0--rc2-0d6efc?labelColor=001d38&style=flat-square)](https://git.drupalcode.org/project/varbase_i18n_base/-/pipelines?ref=1.0.0-rc2)
[![Automated Functional Testing](https://git.drupalcode.org/project/varbase_project/badges/11.0.x/pipeline.svg)](https://git.drupalcode.org/project/varbase_project/-/pipelines)

A recipe to manage internationalization, languages, and translation support with default configurations and permissions for Varbase multilingual sites.

## Description

Varbase Internationalization Base provides comprehensive multilingual support for Drupal sites.

This recipe provides essential internationalization features including:
- **language**: Core language management
- **locale**: Interface translation and localization
- **config_translation**: Configuration translation capabilities
- **content_translation**: Content entity translation support
- **eca**: Event-Condition-Action framework
- **eca_language**: Language-specific ECA events and actions

Drupal Canvas pages are translated with Drupal Canvas's own multilingual support: the recipe enables
content translation for the Drupal Canvas `Page` entity and marks its component input values
translatable, so a page can be translated as soon as a second language is added.

The recipe also ships a translation toolkit in the codebase **without enabling any of it**, so each
site turns on only what it needs:

- **Translation Management Tool (TMGMT)**: translation jobs, local translators and translation
  providers.

  ```
  drush en tmgmt tmgmt_content tmgmt_config tmgmt_local
  ```

- **AI Translation Management Tool (`ai_tmgmt`)**: machine translation through the Drupal AI module,
  offered as a TMGMT provider. Needs an AI provider and model configured first.

  ```
  drush en ai_tmgmt
  ```

The core Translate tab reaches a Drupal Canvas page's title, URL alias, description and metatags
only. Translating the copy inside components is done through a TMGMT job.

## Installation

This is a Drupal recipe that can be applied using Drupal's recipe system.

## Features

- Complete language management system
- Interface and content translation capabilities
- Configuration translation for site settings
- Role-based translation permissions
- Drupal Canvas page translation through Drupal Canvas's own multilingual support, with content
  translation enabled for the Drupal Canvas `Page` entity and its component input values
- Translation Management Tool and AI machine translation available on demand, neither enabled by
  default
- ECA integration for language-based workflows

## Maintainers

- [Vardot](https://www.drupal.org/vardot)

## License

GPL-2.0-or-later
