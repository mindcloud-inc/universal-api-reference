# List All Users with JustCall

Retrieves users from JustCall.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2.1/users`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [List All Users](https://developer.justcall.io/reference/users_list_v21)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `available` | query | `boolean` | no | Filter users by availability. |
| `email` | query | `string` | no | Filter users by email address. |
| `group_id` | query | `number` | no | Filter users by group ID. |
| `order` | query | `string` | no | Sort direction for the returned users. |
| `role` | query | `string` | no | Filter users by role. |
