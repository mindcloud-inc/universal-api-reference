# Retrieve User Availabilities with Vyte

Retrieves a user's availabilities from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/users/:user_id/availabilities`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [Retrieve User Availabilities](https://developer.vyte.in/reference/availabilities/#retrieve-user-availabilities)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | no | The Vyte user ID. |
