# Update a user with WorkOS

Updates a user in your WorkOS environment.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user_management/users/{id}`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Update a user](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the user. |
| `email` | body | `string` | no | The email address of the user. |
| `first_name` | body | `string` | no | The first name of the user. |
| `last_name` | body | `string` | no | The last name of the user. |
| `email_verified` | body | `boolean` | no | Whether the user's email has been verified. |
| `password` | body | `string` | no | The password to set for the user. |
| `password_hash` | body | `string` | no | The hashed password to set for the user. Mutually exclusive with `password`. |
| `password_hash_type` | body | `string` | no | The algorithm originally used to hash the password, used when providing a `password_hash`. |
| `metadata` | body | `object` | no | Object containing metadata key/value pairs associated with the user. |
| `external_id` | body | `string` | no | The external ID of the user. |
| `locale` | body | `string` | no | The user's preferred locale. |
