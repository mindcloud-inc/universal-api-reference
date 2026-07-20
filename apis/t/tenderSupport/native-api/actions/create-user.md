# Create User with Tender Support

Creates a new user in Tender Support.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.tenderapp.com/help`
- **Official documentation:** [Create User](https://help.tenderapp.com/kb/api/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The user's email address. |
| `password` | body | `string` | yes | The user's password. |
| `password_confirmation` | body | `string` | yes | The password confirmation. |
| `name` | body | `string` | no | The user's name. |
| `title` | body | `string` | no | The user's job title. |
