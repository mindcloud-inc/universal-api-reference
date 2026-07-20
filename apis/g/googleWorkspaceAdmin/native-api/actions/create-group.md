# Create Group with Google Workspace Admin

Creates a new group in Google Workspace Admin.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/directory/v1/groups`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Create Group](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the group. |
| `email` | body | `string` | yes | Primary email address for the group. |
| `name` | body | `string` | no | Display name for the group. |
