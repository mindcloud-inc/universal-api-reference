# Create User with CompanyCam

Create a new user in CompanyCam.

## Endpoint

- **Method:** `POST`
- **Path:** `users`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Create User](https://docs.companycam.com/reference/createuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `object` | no | — |
| `user.first_name` | body | `string` | no | — |
| `user.last_name` | body | `string` | no | — |
| `user.email_address` | body | `string` | no | — |
| `user.phone_number` | body | `string` | no | — |
| `user.password` | body | `string` | no | — |
| `user.user_role` | body | `list<string>` | no | Role for the user.  Allowed values: `standard` (default), `restricted` |
