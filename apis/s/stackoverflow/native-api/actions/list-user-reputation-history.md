# List User Reputation History with Stackoverflow

Retrieves reputation history for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/reputation-history`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Reputation History](https://api.stackexchange.com/docs/reputation-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose reputation history to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
