# Add Workspace User with OpnForm

Adds a user to an OpnForm workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/workspaces/:workspaceId/users/add`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Add Workspace User](https://docs.opnform.com/api-reference/workspace-users/add-workspace-user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `email` | body | `string` | yes |
| `role` | body | `string` | yes |
