# Create I18n Translation Job with TranslatePlus

Creates a new i18n translation job in TranslatePlus.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/translate/i18n`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Create I18n Translation Job](https://docs.translateplus.io/reference/v2/i18n/i18n-create-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Upload a JSON, YAML, CSV, Properties, or XML localization file. |
| `source_language` | body | `string` | no | — |
| `target_languages` | body | `string` | yes | Comma-separated target language codes such as fr,de. |
| `webhook_url` | body | `string` | no | Optional URL that receives job-completion callbacks. |
