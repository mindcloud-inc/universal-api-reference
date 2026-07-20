# Create User with Swit

Creates a new user in Swit.

## Endpoint

- **Method:** `POST`
- **Path:** `organization.user.create`
- **Base URL:** `https://openapi.swit.io`
- **Official documentation:** [Create User](https://tech-support.swit.io/books/swit-java-development-guide/page/6512b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | no | Language for the new user. |
| `timezone` | body | `string` | no | Timezone for the new user. |
| `user_name` | body | `string` | yes | Display name for the user. |
| `user_email` | body | `string` | yes | Email address for the user. |
| `tel` | body | `string` | no | Telephone number for the user. |
| `msg` | body | `string` | no | Optional profile message for the user. |
