# Delete Group with Google Workspace Admin

Deletes an existing group from Google Workspace Admin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/directory/v1/groups/:groupKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Delete Group](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
