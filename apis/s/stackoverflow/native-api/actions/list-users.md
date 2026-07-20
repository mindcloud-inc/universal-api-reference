# List Users with Stackoverflow

Retrieves users from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Users](https://api.stackexchange.com/docs/users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
