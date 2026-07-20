# Get GIF by ID with Giphy

Retrieves a GIF from Giphy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/gifs/:gifId`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Get GIF by ID](https://developers.giphy.com/docs/api/endpoint/#get-gif-by-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `gifId` | path | `string` | yes |
| `rating` | query | `string` | no |
