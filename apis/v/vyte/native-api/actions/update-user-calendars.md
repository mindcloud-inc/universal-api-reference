# Update User Calendars with Vyte

Updates a user's calendars in Vyte.

## Endpoint

- **Method:** `PUT`
- **Path:** `v2/users/:user_id/calendars`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [Update User Calendars](https://developer.vyte.in/reference/calendars/#update-user-calendars)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | no | The Vyte user ID. |
