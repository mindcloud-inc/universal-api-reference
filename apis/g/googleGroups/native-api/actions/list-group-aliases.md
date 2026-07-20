# List Group Aliases with Google Groups

Retrieves aliases for a group from Google Groups.

## Endpoint

- **Method:** `GET`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [List Group Aliases](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups.aliases/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
