# Get User Photo with Google Workspace Admin

Retrieves a user's photo from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/users/:userKey/photos/thumbnail`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Get User Photo](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.photos/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
