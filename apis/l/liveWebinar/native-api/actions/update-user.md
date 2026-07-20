# Update User with LiveWebinar

Updates an existing user in LiveWebinar.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/users/:user_id`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Update User](https://docs.archiebot.com/?version=latest#4414eb9b-a67e-4146-9a47-8fde3e97ad84)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `confirmed` | body | `string` | no |
| `country_code_iso2` | body | `string` | no |
| `country_state_iso2` | body | `string` | no |
| `email` | body | `string` | yes |
| `package_id` | body | `string` | no |
| `password` | body | `string` | no |
| `status` | body | `string` | no |
| `user_id` | path | `string` | yes |
