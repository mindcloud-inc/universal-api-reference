# Update user with Good Grants

Updates an existing user in Good Grants.

## Endpoint

- **Method:** `PUT`
- **Path:** `user/:slug`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Update user](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | User slug |
| `first_name` | body | `string` | no | User first name |
| `last_name` | body | `string` | no | User last name |
| `password` | body | `string` | no | User password |
| `email` | body | `string` | no | User email |
| `mobile` | body | `string` | no | User mobile number |
| `roles[]` | body | `array<string>` | no | Role slugs |
| `preferences` | body | `object` | no | Notification preferences |
| `user_fields` | body | `object` | no | Field slug to value map |
