# Check Group Membership with Google Workspace Admin

Checks whether a user belongs to a group in Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/groups/:groupKey/hasMember/:memberKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Check Group Membership](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/hasMember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `memberKey` | path | `string` | yes | Member email address, alias, or unique ID. |
