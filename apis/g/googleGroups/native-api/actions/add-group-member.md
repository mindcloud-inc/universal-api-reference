# Add Group Member with Google Groups

Adds a member to a group in Google Groups.

## Endpoint

- **Method:** `POST`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Add Group Member](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `email` | body | `string` | yes | The member's email address. This field is required when adding a member. |
| `role` | body | `string` | no | The member's role in the group, such as MEMBER, MANAGER, or OWNER. |
| `delivery_settings` | body | `string` | no | Email delivery preference for the member, such as ALL_MAIL, DAILY, DIGEST, DISABLED, or NONE. |
