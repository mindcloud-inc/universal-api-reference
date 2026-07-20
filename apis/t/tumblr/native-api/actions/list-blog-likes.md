# List Blog Likes with Tumblr

Retrieves liked posts from a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/likes`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Blog Likes](https://www.tumblr.com/docs/en/api/v2#likes--retrieve-blogs-likes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | The blog whose public likes should be retrieved. |
| `before` | query | `number` | no | Retrieve likes before the specified Unix timestamp. |
| `after` | query | `number` | no | Retrieve likes after the specified Unix timestamp. |
