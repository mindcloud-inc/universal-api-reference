# List Changed Posts By Media Type with Walls.io

Finds updated posts in Walls.io by media type.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/changed`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Changed Posts By Media Type](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md)

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
| `since` | query | `string` | no | UNIX timestamp; returns posts changed after this time. |
