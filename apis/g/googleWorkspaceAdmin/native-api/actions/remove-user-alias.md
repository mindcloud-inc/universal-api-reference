# Remove User Alias with Google Workspace Admin

Deletes a user alias from Google Workspace Admin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/directory/v1/users/:userKey/aliases/:alias`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Remove User Alias](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.aliases/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
| `alias` | path | `string` | yes | Alias email address to remove. |
