# List Video Categories with YouTube

Retrieves available video categories from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/videoCategories`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Video Categories](https://developers.google.com/youtube/v3/docs/videoCategories/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated videoCategory resource parts to include. |
| `regionCode` | query | `string` | no | ISO 3166-1 alpha-2 region code. |
| `id` | query | `string` | no | Comma-separated list of video category IDs. |
| `hl` | query | `string` | no | UI language code for localized metadata. |
