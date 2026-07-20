# Get GIFs by ID with Giphy

Retrieves multiple GIFs from Giphy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/gifs`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Get GIFs by ID](https://developers.giphy.com/docs/api/endpoint/#get-gifs-by-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids` | query | `string` | yes |
| `rating` | query | `string` | no |
