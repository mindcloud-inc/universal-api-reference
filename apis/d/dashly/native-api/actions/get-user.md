# Get User with Dashly

Retrieves a Dashly user by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Get User](https://developers.dashly.io/webapi/endpoints/users/user/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Dashly ID or your external User ID. |
| `by_user_id` | query | `boolean` | no | Interpret the identifier as your external User ID. |
| `id_as_string` | query | `boolean` | no | — |
