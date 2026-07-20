# Check Group Membership with Google Groups

Checks whether a member belongs to a group in Google Groups.

## Endpoint

- **Method:** `GET`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/hasMember/:memberKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Check Group Membership](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/hasMember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `memberKey` | path | `string` | yes | The member email address or unique member ID. |
