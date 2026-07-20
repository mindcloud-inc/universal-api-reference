# Create user with Good Grants

Creates a new user in Good Grants.

## Endpoint

- **Method:** `POST`
- **Path:** `user`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Create user](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | User first name |
| `last_name` | body | `string` | yes | User last name |
| `password` | body | `string` | yes | User password |
| `email` | body | `string` | no | User email |
| `mobile` | body | `string` | no | User mobile number |
| `roles[]` | body | `array<string>` | no | Role slugs |
| `preferences` | body | `object` | no | Notification preferences |
| `user_fields` | body | `object` | no | Field slug to value map |
