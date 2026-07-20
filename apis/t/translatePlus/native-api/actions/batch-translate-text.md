# Batch Translate Text with TranslatePlus

Translates multiple texts in one TranslatePlus request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/translate/batch`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Batch Translate Text](https://docs.translateplus.io/reference/v2/translation/batch-translate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `texts[]` | body | `array<string>` | yes |
| `source` | body | `string` | yes |
| `target` | body | `string` | yes |
