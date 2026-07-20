# List User Likes with Tumblr

Retrieves posts liked by the Tumblr user.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/user/likes`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List User Likes](https://www.tumblr.com/docs/en/api/v2#userlikes--retrieve-a-users-likes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `number` | no | Retrieve posts liked before the specified timestamp. |
| `after` | query | `number` | no | Retrieve posts liked after the specified timestamp. |
