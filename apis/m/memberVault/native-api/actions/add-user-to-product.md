# Add User to Product with MemberVault

Adds a user to a MemberVault product, creating them if needed.

## Endpoint

- **Method:** `GET`
- **Path:** `/add_user`
- **Base URL:** `https://{accountName}.mvsite.app/api`
- **Official documentation:** [Add User to Product](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_key` | query | `string` | yes | The MemberVault course key for the target course. |
| `email` | query | `string` | yes | The email address for the user to add. |
| `first_name` | query | `string` | yes | The user's first name. |
| `last_name` | query | `string` | yes | The user's last name. |
