# Translate HTML with TranslatePlus

Translates HTML content in TranslatePlus while preserving structure.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/translate/html`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Translate HTML](https://docs.translateplus.io/reference/v2/translation/translate-html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `html` | body | `string` | yes |
| `source` | body | `string` | yes |
| `target` | body | `string` | yes |
