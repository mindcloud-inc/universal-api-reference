# Retrieve User with Vyte

Retrieves a user from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/users/:user_id`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [Retrieve User](https://developer.vyte.in/reference/users/#retrieve-a-user)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | The Vyte user ID. |
