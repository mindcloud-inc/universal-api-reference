# List User Aliases with Google Workspace Admin

Retrieves a user's aliases from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/users/:userKey/aliases`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [List User Aliases](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.aliases/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
