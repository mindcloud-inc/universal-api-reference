# List User Questions with Stackoverflow

Retrieves questions for specific users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/[:ids]/questions`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List User Questions](https://api.stackexchange.com/docs/questions-on-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited user IDs whose questions to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
