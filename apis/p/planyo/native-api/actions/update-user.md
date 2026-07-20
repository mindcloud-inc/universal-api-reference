# Update User with Planyo

Updates an existing user in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Update User](https://www.planyo.com/api.php?topic=modify_user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | query | `number` | no |
| `email` | query | `string` | no |
| `user_login` | query | `string` | no |
| `first_name` | query | `string` | no |
| `last_name` | query | `string` | no |
| `new_email` | query | `string` | no |
| `email_verified` | query | `boolean` | no |
| `city` | query | `string` | no |
| `country` | query | `string` | no |
| `user_language` | query | `string` | no |
| `is_preapproved` | query | `boolean` | no |
| `is_banned` | query | `boolean` | no |
| `site_id` | query | `number` | no |
