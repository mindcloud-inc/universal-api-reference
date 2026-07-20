# Get Users with Stackoverflow

Retrieves specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Users](https://api.stackexchange.com/docs/users-by-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-separated Stack Exchange user IDs. |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
