# Delete User Calendar with Vyte

Deletes a user's calendar from Vyte.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v2/users/:user_id/calendars/:calendar_id`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [Delete User Calendar](https://developer.vyte.in/reference/calendars/#delete-user-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar_id` | path | `string` | no | The Vyte calendar ID. |
| `user_id` | path | `string` | no | The Vyte user ID. |
