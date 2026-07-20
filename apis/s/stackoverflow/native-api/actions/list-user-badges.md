# List User Badges with Stackoverflow

Retrieves badges for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/badges`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Badges](https://api.stackexchange.com/docs/badges-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose badges to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
