# Update Group with Clockify

Updates an existing user group in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/user-groups/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Group](https://docs.developer.clockify.me/#tag/Group/operation/updateUserGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `workspaceId` | path | `list<string>` | yes |
