# Delete User with Google Workspace Admin

Deletes an existing user from Google Workspace Admin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/directory/v1/users/:userKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Delete User](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
