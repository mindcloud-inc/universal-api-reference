# List User Timeline with Stackoverflow

Retrieves timeline entries for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/timeline`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Timeline](https://api.stackexchange.com/docs/timeline-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose timeline to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
