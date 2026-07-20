# Create User with TeamBook

Creates a new user in TeamBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://web.teambookapp.com/api/public`
- **Official documentation:** [Create User](https://kb.teambookapp.com/en/article/create-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The user's first name. |
| `last_name` | body | `string` | yes | The user's last name. |
| `email` | body | `string` | yes | The user's email address. |
| `role` | body | `string` | yes | The TeamBook role for the user. |
| `billable` | body | `boolean` | yes | Whether the user is billable. |
