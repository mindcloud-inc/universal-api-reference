# List User Calendars with Vyte

Retrieves a user's calendars from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/users/:user_id/calendars`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [List User Calendars](https://developer.vyte.in/reference/calendars/#list-user-calendars)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | no | The Vyte user ID. |
