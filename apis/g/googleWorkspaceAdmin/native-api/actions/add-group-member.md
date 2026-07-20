# Add Group Member with Google Workspace Admin

Adds a member to a Google Workspace Admin group.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/directory/v1/groups/:groupKey/members`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Add Group Member](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delivery_settings` | body | `string` | no | Optional delivery setting for email delivery to this member. |
| `email` | body | `string` | yes | Email address of the member to add. |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `role` | body | `string` | no | Role to assign: OWNER, MANAGER, or MEMBER. |
| `type` | body | `string` | no | Member type such as USER or GROUP. |
