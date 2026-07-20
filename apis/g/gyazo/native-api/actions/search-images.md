# Search Images with Gyazo

Finds images in Gyazo by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search`
- **Base URL:** `https://api.gyazo.com`
- **Official documentation:** [Search Images](https://gyazo.com/api/docs/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text, maximum 200 characters. |
| `page` | query | `number` | no | Page number. |
| `per` | query | `number` | no | Number of results per page, maximum 100. |
