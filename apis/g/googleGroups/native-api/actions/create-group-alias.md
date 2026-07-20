# Create Group Alias with Google Groups

Creates a group alias in Google Groups.

## Endpoint

- **Method:** `POST`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Create Group Alias](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups.aliases/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `alias` | body | `string` | yes | The editable alias email address to add to the group. |
