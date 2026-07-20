# Delete Group with Google Groups

Deletes an existing group from Google Groups.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Delete Group](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
