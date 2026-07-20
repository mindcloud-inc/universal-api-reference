# Create User with Helpjuice

Creates a new user in Helpjuice.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create User](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The Helpjuice user email. |
| `first_name` | body | `string` | no | The Helpjuice user first name. |
| `last_name` | body | `string` | no | The Helpjuice user last name. |
| `role_id` | body | `string` | yes | The Helpjuice role id for the user. Observed valid values include viewer and admin. |
| `user` | body | `object` | no | — |
