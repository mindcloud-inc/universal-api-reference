# Export Translations with SimpleLocalize

Exports translations from SimpleLocalize as files.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v4/export`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Export Translations](https://api.simplelocalize.io/openapi/ui#/File%20import%20%26%20export/exportTranslations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadFormat` | query | `list` | no | Accepted values: `android`, `android-strings`, `android-xml`, `csv-translations`, `excel`, `java-properties`, `javascript`, `localizable-strings`, `localizable-strings-dict`, `localizable-xcstrings`, `module-exports`, `multi-language-json`, `php-array`, `po-pot`, `qt-linguist`, `resx`, `simplelocalize-json`, `single-language-json`, `string-resources`, `tsv`, `yaml`. |
| `downloadOptions[]` | query | `array<string>` | no | — |
| `languageKeys[]` | query | `array<string>` | no | — |
| `tags[]` | query | `array<string>` | no | — |
| `languageOrder[]` | query | `array<string>` | no | — |
| `customerId` | query | `string` | no | — |
| `sort` | query | `list` | no | Accepted values: `DEFAULT`, `IMPORT_ORDER`, `NAMESPACES`, `NEWEST_KEYS_FIRST`, `NEWEST_KEYS_LAST`. |
