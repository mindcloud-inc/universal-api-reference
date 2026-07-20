# List Posts By Media Type with Walls.io

Finds posts in Walls.io by media type.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Posts By Media Type](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_types` | query | `string` | no | Comma-separated list of media types to include. |
