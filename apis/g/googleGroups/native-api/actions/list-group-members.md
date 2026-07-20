# List Group Members with Google Groups

Retrieves members of a group from Google Groups.

## Endpoint

- **Method:** `GET`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [List Group Members](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
