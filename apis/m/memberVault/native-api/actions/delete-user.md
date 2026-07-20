# Delete User with MemberVault

Deletes a user and their data from MemberVault.

## Endpoint

- **Method:** `GET`
- **Path:** `/delete_user`
- **Base URL:** `https://{accountName}.mvsite.app/api`
- **Official documentation:** [Delete User](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address for the user to delete. |
