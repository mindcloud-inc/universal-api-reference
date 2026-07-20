# Create User with LiveWebinar

Creates a new user in LiveWebinar.

## Endpoint

- **Method:** `POST`
- **Path:** `api/users`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Create User](https://docs.archiebot.com/?version=latest#bac4389f-4fde-4fe7-a945-f82f745bbb12)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `confirmed` | body | `string` | no |
| `country_code_iso2` | body | `string` | no |
| `country_state_iso2` | body | `string` | no |
| `created_ip` | body | `string` | no |
| `data_location` | body | `string` | no |
| `email` | body | `string` | yes |
| `package_id` | body | `string` | no |
| `password` | body | `string` | yes |
| `status` | body | `string` | no |
