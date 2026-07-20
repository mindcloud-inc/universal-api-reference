# Update Workspace User Role with OpnForm

Updates a user's role in an OpnForm workspace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open/workspaces/:workspaceId/users/:userId/update-role`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Update Workspace User Role](https://docs.opnform.com/api-reference/workspace-users/update-workspace-user-role)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `userId` | path | `number` | yes |
| `role` | body | `string` | yes |
