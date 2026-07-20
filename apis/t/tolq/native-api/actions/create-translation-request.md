# Create Translation Request with Tolq

Creates a translation request in Tolq.

## Endpoint

- **Method:** `POST`
- **Path:** `/translations/requests`
- **Base URL:** `https://api.tolq.com/v1`
- **Official documentation:** [Create Translation Request](https://docs.tolq.com/reference/post-a-translation-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | Tolq request object containing the translatable keys and nested text values. |
| `source_language_code` | body | `string` | yes | Two-letter ISO 639-1 source language code. |
| `target_language_code` | body | `string` | yes | Two-letter ISO 639-1 target language code. |
| `quality` | body | `string` | yes | Tolq quality level: machine, postediting, translation, localization, or expert. |
