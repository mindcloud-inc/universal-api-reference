# Remove Workspace User with OpnForm

Removes a user from an OpnForm workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/open/workspaces/:workspaceId/users/:userId/remove`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Remove Workspace User](https://docs.opnform.com/api-reference/workspace-users/remove-workspace-user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `userId` | path | `number` | yes |
