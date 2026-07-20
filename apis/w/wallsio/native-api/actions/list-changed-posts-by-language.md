# List Changed Posts By Language with Walls.io

Finds updated posts in Walls.io by language.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/changed`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Changed Posts By Language](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languages` | query | `string` | no | Comma-separated ISO 639-1 language codes to include. |
| `since` | query | `string` | no | UNIX timestamp; returns posts changed after this time. |
