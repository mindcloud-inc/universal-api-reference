# Translate Subtitles with TranslatePlus

Translates subtitle files in TranslatePlus while preserving timing.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/translate/subtitles`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Translate Subtitles](https://docs.translateplus.io/reference/v2/translation/translate-subtitles)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `format` | body | `string` | yes |
| `content` | body | `string` | yes |
| `source` | body | `string` | yes |
| `target` | body | `string` | yes |
