# Create User with 5pm

Creates a new user in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/users/add`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Create User](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user[firstName]` | query | `string` | yes | First name of the user to create. |
| `user[securityLevel]` | query | `string` | yes | — |
| `user[email]` | query | `string` | yes | — |
| `user[password]` | query | `string` | yes | — |
