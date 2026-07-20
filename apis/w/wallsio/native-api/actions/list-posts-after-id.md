# List Posts After ID with Walls.io

Finds posts in Walls.io after a post ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Posts After ID](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return only posts with a higher Walls.io post ID than this value. |
