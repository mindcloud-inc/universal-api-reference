# Get Post With Source with Walls.io

Retrieves a post with source details from Walls.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/:postId`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [Get Post With Source](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-postid.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postId` | path | `string` | no | Walls.io post ID. |
