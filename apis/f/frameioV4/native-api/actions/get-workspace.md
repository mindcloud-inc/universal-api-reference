# Get Workspace with Frame.io v4

Retrieves a workspace from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/workspaces/:workspaceId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get Workspace](https://next.developer.frame.io/platform/api-reference/workspaces/show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `workspace_id` | path | `string` | yes |
| `include` | query | `string` | no |
