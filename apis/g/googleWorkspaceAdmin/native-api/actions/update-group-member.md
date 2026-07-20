# Update Group Member with Google Workspace Admin

Updates a member in a Google Workspace Admin group.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/directory/v1/groups/:groupKey/members/:memberKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Update Group Member](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delivery_settings` | body | `string` | no | Optional delivery setting for email delivery to this member. |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `memberKey` | path | `string` | yes | Member email address, alias, or unique ID. |
| `role` | body | `string` | no | Role to assign: OWNER, MANAGER, or MEMBER. |
| `type` | body | `string` | no | Member type such as USER or GROUP. |
