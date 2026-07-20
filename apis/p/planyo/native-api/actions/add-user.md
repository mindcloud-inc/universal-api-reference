# Add User with Planyo

Creates a new user in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Add User](https://www.planyo.com/api.php?topic=add_user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `first_name` | query | `string` | yes |
| `last_name` | query | `string` | no |
| `user_login` | query | `string` | no |
| `user_password` | query | `string` | no |
| `country` | query | `string` | no |
| `city` | query | `string` | no |
| `user_language` | query | `string` | no |
| `admin_user_id` | query | `number` | no |
