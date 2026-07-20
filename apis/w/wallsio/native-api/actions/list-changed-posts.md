# List Changed Posts with Walls.io

Retrieves posts updated since a timestamp from Walls.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/changed`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Changed Posts](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `string` | no | UNIX timestamp; returns posts changed after this time. |
