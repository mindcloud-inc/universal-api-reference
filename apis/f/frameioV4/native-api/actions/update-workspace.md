# Update Workspace with Frame.io v4

Updates an existing workspace in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/workspaces/:workspaceId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Update Workspace](https://next.developer.frame.io/platform/api-reference/workspaces/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `workspace_id` | path | `string` | yes |
| `data` | body | `object` | yes |
