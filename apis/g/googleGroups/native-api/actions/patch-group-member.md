# Patch Group Member with Google Groups

Updates an existing group member in Google Groups.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Patch Group Member](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `memberKey` | path | `string` | yes | The member email address or unique member ID. |
| `role` | body | `string` | no | The member's role in the group, such as MEMBER, MANAGER, or OWNER. |
| `delivery_settings` | body | `string` | no | Email delivery preference for the member, such as ALL_MAIL, DAILY, DIGEST, DISABLED, or NONE. |
