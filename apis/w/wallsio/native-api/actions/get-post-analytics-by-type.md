# Get Post Analytics By Type with Walls.io

Retrieves post counts for selected post types from Walls.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/posts`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [Get Post Analytics By Type](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_analytics-posts.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `types` | query | `string` | no | Comma-separated list of post types to count. |
