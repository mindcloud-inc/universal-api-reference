# Admin Create User with Bonusly

Creates a new user in Bonusly.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Admin Create User](https://docs.bonus.ly/reference/admin-create-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The user's email address. |
| `first_name` | body | `string` | yes | The user's first name. |
| `last_name` | body | `string` | yes | The user's last name. |
