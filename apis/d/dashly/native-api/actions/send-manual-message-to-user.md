# Send Manual Message To User with Dashly

Sends a manual message to a Dashly user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:id/sendmessage`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Send Manual Message To User](https://developers.dashly.io/webapi/endpoints/users/sendmessage/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `by_user_id` | query | `boolean` | no |
| `body` | body | `string` | yes |
| `id_as_string` | query | `boolean` | no |
| `type` | body | `string` | no |
