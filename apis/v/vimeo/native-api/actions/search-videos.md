# Search Videos with Vimeo

Finds videos in Vimeo by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Search Videos](https://developer.vimeo.com/api/reference/videos#search_videos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | The search query. |
| `filter` | query | `list` | no | The attribute by which to filter the results. Accepted values: `CC`, `CC-BY`, `CC-BY-NC`, `CC-BY-NC-ND`, `CC-BY-NC-SA`, `CC-BY-ND`, `CC-BY-SA`, `CC0`, `categories`, `duration`, `in-progress`, `minimum_likes`, `trending`, `upload_date`. |
| `links` | query | `string` | no | A comma-separated list of video URLs to find. |
| `uris` | query | `string` | no | A comma-separated list of video URIs to find. |
