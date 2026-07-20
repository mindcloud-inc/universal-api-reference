# Delete Group Alias with Google Groups

Deletes a group alias from Google Groups.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases/:alias`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Delete Group Alias](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups.aliases/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `alias` | path | `string` | yes | The alias email address to delete from the group. |
