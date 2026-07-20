# Get Group Member with Google Groups

Retrieves a group member from Google Groups.

## Endpoint

- **Method:** `GET`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Get Group Member](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `memberKey` | path | `string` | yes | The member email address or unique member ID. |
