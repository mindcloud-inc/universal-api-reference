# List users with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List users](https://developer-docs.gomotive.com/reference/list-all-the-users-of-a-company)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | query | `string` | no | Filter users by role. |
| `duty_status` | query | `string` | no | Filter drivers by duty status. |
| `status` | query | `string` | no | Filter users by status. |
| `name` | query | `string` | no | Filter users by first name, last name, or both. |
| `updated_after` | query | `date` | no | Return users updated after the given date. |
