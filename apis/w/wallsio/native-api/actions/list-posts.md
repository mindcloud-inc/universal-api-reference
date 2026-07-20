# List Posts with Walls.io

Retrieves posts from Walls.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.walls.io/v1`
- **Official documentation:** [List Posts](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of posts to return. Maximum 1000. |
| `include_inactive` | query | `boolean` | no | Include inactive posts when set. |
| `pinned_only` | query | `boolean` | no | Return only posts pinned to the top of the wall. |
| `fields` | query | `string` | no | Comma-separated list of post fields to include. |
| `sort` | query | `string` | no | Comma-separated sort fields. Prefix a field with - for descending. |
