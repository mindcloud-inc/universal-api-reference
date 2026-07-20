# Import Translations with SimpleLocalize

Imports translations from a file into SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/import`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Import Translations](https://api.simplelocalize.io/openapi/ui#/File%20import%20%26%20export/importTranslations)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploadFormat` | query | `list` | yes | Accepted values: `android`, `android-strings`, `android-xml`, `csv-translations`, `excel`, `java-properties`, `javascript`, `localizable-strings`, `localizable-strings-dict`, `localizable-xcstrings`, `module-exports`, `multi-language-json`, `php-array`, `po-pot`, `qt-linguist`, `resx`, `simplelocalize-json`, `single-language-json`, `string-resources`, `tsv`, `yaml`. |
| `importOptions[]` | query | `array<string>` | no | — |
| `languageKey` | query | `string` | no | — |
| `customerId` | query | `string` | no | — |
| `namespace` | query | `string` | no | — |
| `tags[]` | query | `array<string>` | no | — |
