# Add User Alias with Google Workspace Admin

Adds a user alias in Google Workspace Admin.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/directory/v1/users/:userKey/aliases`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Add User Alias](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.aliases/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
| `alias` | body | `string` | yes | New alias email address to add for the user. |
