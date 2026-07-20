# List User Reputation with Stackoverflow

Retrieves reputation changes for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/reputation`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Reputation](https://api.stackexchange.com/docs/reputation-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose reputation changes to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
