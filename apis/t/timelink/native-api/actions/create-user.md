# Create User with Timelink

Creates a user in the Timelink workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Create User](https://api.timelink.io/documentation#/Users/post_api_v1_users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The user's first name. |
| `last_name` | body | `string` | yes | The user's last name. |
| `email` | body | `string` | yes | The user's email address. |
| `active` | body | `boolean` | no | Whether the user is active. |
| `admin` | body | `number` | no | Admin level. Docs say 9 makes the user an admin. |
