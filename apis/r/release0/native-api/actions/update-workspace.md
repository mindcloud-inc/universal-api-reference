# Update Workspace with Release0

Updates a workspace in Release0.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/workspaces/:workspaceId`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Update Workspace](https://docs.release0.com/api-reference/workspace/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The workspace name. |
| `slug` | body | `string` | no | The workspace slug. |
| `workspaceId` | path | `string` | yes | The workspace ID. |
