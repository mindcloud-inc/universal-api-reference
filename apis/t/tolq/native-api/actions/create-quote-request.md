# Create Quote Request with Tolq

Creates a quote request in Tolq.

## Endpoint

- **Method:** `POST`
- **Path:** `/translations/requests/quote`
- **Base URL:** `https://api.tolq.com/v1`
- **Official documentation:** [Create Quote Request](https://docs.tolq.com/reference/create-a-quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | Tolq request object containing the translatable keys and nested text values. |
| `source_language_code` | body | `string` | yes | Two-letter ISO 639-1 source language code. |
| `target_language_code` | body | `string` | yes | Two-letter ISO 639-1 target language code. |
| `quality` | body | `string` | yes | Tolq quality level: machine, postediting, translation, localization, or expert. |
