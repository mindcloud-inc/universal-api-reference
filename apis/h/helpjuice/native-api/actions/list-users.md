# List Users with Helpjuice

Retrieves users from Helpjuice.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Users](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[role]` | query | `string` | no | Filter users by role. |
| `filter[email]` | query | `string` | no | Filter users by email. |
| `filter[name]` | query | `string` | no | Filter users by display name. |
