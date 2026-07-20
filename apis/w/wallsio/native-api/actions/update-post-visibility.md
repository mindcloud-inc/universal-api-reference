# Update Post Visibility with Walls.io

Updates a post visibility status in Walls.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:postId`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [Update Post Visibility](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postId` | path | `string` | no | Walls.io post ID. |
| `status` | body | `string` | no | Set to 1 to show the post or 0 to hide it. |
