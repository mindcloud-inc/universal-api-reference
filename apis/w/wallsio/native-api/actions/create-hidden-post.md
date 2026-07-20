# Create Hidden Post with Walls.io

Creates a new hidden post in Walls.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [Create Hidden Post](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/POST_posts.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | Text content for the native post. |
| `user_name` | body | `string` | no | Display name shown for the native post author. |
