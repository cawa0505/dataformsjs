# Internationalization (I18N) - Language Translations

## Overview

This document provides a brief overview of changes needed when adding new languages to DataFormsJS. Three different repositories need to be updated for full site translations.

The following setup is recommended for local development.

~~~
dataformsjs {root-directory}
├── dataformsjs [repository]
├── playground [repository]
└── website [repository]
~~~

If you need to install PHP see documents for (Windows, macOS, and Linux) from: https://www.fastsitephp.com/en/getting-started

Currently specific languages are desired and translation work can be paid. For more see: https://www.fastsitephp.com/en/translators-needed

Google Translate is used for initial translations and then human translators fix errors from Google Translate.

## JSON Files

Files for specific languages end with `*.{lang}.json` and the main files for the main site is `_.{lang}.json`.

* `dataformsjs\examples\i18n`
* `website\public\i18n`

https://github.com/dataformsjs/dataformsjs/tree/master/examples/i18n
https://github.com/dataformsjs/website/tree/master/public/i18n

## Related HTML Files

https://github.com/dataformsjs/website/blob/master/app/Views/index.htm

See line #5: `data-i18n-locales="en,..."`. Once all JSON files are created copy the full text for the [data-i18n-locales] attribute and then find/replace globally in all files using a Code Editor. As of 12/2019 there are 30 instances in 12 files.

# Code Playground Template

Each language has it's own template directory/folder. Text content and code comments are updated to the translated language.

`playground\app_data\template\{lang}`

https://github.com/dataformsjs/playground/tree/master/app_data/template

## Code Playground Language Whitelist

PHP code has to be updated so the language can be used.

https://github.com/dataformsjs/playground/blob/master/app/app.php

Line 49: `function getLangauage($lang) {`

## Main Site Readme

Some of this content is duplicated from the main home page so some content simply be copied after translating JSON files.

`dataformsjs\docs\i18n-readme\README.{lang}.md`

https://github.com/dataformsjs/dataformsjs/tree/master/docs/i18n-readme

## Quick Reference Code

Code comments are updated to the translated language.

`website\app_data\example-code\quick-reference-{lang}.htm`

https://github.com/dataformsjs/website/tree/master/app_data/example-code