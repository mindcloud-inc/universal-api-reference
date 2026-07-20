# Get User with Google Workspace Admin

Retrieves a user from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/users/:userKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Get User](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
