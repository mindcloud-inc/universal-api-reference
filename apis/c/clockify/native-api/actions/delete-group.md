# Delete Group with Clockify

Deletes an existing user group from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/user-groups/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Group](https://docs.developer.clockify.me/#tag/Group/operation/deleteUserGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |
