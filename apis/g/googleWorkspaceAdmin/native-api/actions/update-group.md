# Update Group with Google Workspace Admin

Updates an existing group in Google Workspace Admin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/directory/v1/groups/:groupKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Update Group](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the group. |
| `email` | body | `string` | no | Primary email address for the group. |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `name` | body | `string` | no | Display name for the group. |
