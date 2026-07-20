# Update My Account with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:user_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update My Account](https://superthread.com/docs/api-docs/users/update-my-account)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | path | `string` | yes |
| `display_name` | body | `string` | no |
| `timezone_id` | body | `string` | no |
| `autodetect_timezone_id` | body | `boolean` | no |
