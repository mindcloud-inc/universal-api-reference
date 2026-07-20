# List Users with FireHydrant

Retrieves users from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Users](https://docs.firehydrant.com/reference/list_users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter users by name. |
| `query` | query | `string` | no | Search users by name. |
