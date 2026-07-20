# List User Answers with Stackoverflow

Retrieves answers for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/answers`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Answers](https://api.stackexchange.com/docs/answers-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose answers to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
