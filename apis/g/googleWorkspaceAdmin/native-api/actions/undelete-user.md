# Undelete User with Google Workspace Admin

Restores a deleted user in Google Workspace Admin.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/directory/v1/users/:userKey/undelete`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Undelete User](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/undelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | The immutable unique ID of the deleted user to restore. |
| `orgUnitPath` | body | `string` | yes | The organizational unit path for the restored user. |
