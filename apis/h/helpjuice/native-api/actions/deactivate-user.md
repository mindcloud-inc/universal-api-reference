# Deactivate User with Helpjuice

Deactivates a user in Helpjuice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id/deactivate`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Deactivate User](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Helpjuice user id. |
| `role_id` | body | `string` | yes | The Helpjuice role id for the user. |
