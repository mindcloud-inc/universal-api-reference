# Remove User From Organization with Vyte

Removes a user from an organization in Vyte.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v2/users/:user_id`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [Remove User From Organization](https://developer.vyte.in/reference/users/#delete-a-user)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | no | The Vyte user ID. |
