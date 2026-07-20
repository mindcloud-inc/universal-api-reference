# Delete Group Member with Google Groups

Deletes an existing group member from Google Groups.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Delete Group Member](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `memberKey` | path | `string` | yes | The member email address or unique member ID. |
