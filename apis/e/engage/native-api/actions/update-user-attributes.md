# Update User Attributes with Engage

Updates a user in Engage, or creates one if missing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:uid`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Update User Attributes](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#update-attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at` | body | `string` | no | The signup or creation timestamp for the user. |
| `device_platform` | body | `string` | no | The device platform, such as android or ios. |
| `device_token` | body | `string` | no | The user’s device token. |
| `email` | body | `string` | no | The user’s email address. |
| `first_name` | body | `string` | no | The user’s first name. |
| `is_account` | body | `boolean` | no | Set to true to convert or create the entity as an account. |
| `last_name` | body | `string` | no | The user’s last name. |
| `meta` | body | `object` | no | Additional user attributes as an object. |
| `number` | body | `string` | no | The user’s phone number in international format. |
| `uid` | path | `string` | yes | The user ID from your application. |
