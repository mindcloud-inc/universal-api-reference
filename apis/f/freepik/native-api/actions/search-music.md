# Search Music with Freepik

Finds Freepik music by search term and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/music`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Search Music](https://docs.freepik.com/api-reference/music/search-music)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Music search query. |
| `limit` | query | `number` | no | Maximum number of music tracks to return. |
| `offset` | query | `number` | no | Zero-based music result offset. |
