# Update User Custom Field with Clockify

Updates a user custom field value in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/users/:userId/custom-field/:customFieldId/value`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update User Custom Field](https://docs.developer.clockify.me/#tag/User/operation/upsertUserCustomFieldValue)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `customFieldId` | path | `string<string>` | yes |
| `value` | body | `object` | no |
