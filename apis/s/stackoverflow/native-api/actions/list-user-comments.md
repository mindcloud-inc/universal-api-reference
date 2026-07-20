# List User Comments with Stackoverflow

Retrieves comments for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/comments`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Comments](https://api.stackexchange.com/docs/comments-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose comments to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
