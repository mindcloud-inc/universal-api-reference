# List User Favorites with Stackoverflow

Retrieves favorite questions for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/favorites`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Favorites](https://api.stackexchange.com/docs/favorites-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose favorite questions to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
