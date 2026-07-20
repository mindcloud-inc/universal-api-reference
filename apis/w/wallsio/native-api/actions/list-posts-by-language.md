# List Posts By Language with Walls.io

Finds posts in Walls.io by language.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Posts By Language](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md)

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
