# Translate Text with TranslatePlus

Translates text between languages in TranslatePlus.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/translate`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Translate Text](https://docs.translateplus.io/reference/v2/translation/translate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `source` | body | `string` | yes |
| `target` | body | `string` | yes |
