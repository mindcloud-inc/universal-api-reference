# Update User with Helpjuice

Updates an existing user in Helpjuice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update User](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | The Helpjuice user first name. |
| `id` | path | `number` | yes | The Helpjuice user id. |
| `last_name` | body | `string` | no | The Helpjuice user last name. |
| `role_id` | body | `string` | no | The Helpjuice role id for the user. |
| `user` | body | `object` | no | — |
