# Remove User from Product with MemberVault

Removes a user's access to a product in MemberVault.

## Endpoint

- **Method:** `GET`
- **Path:** `/remove_user`
- **Base URL:** `https://{accountName}.mvsite.app/api`
- **Official documentation:** [Remove User from Product](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_key` | query | `string` | yes | The MemberVault course key for the target course. |
| `email` | query | `string` | yes | The email address for the user to remove. |
