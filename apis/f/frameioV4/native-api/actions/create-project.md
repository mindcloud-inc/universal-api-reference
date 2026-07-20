# Create Project with Frame.io v4

Creates a new project in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/workspaces/:workspaceId/projects`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create Project](https://next.developer.frame.io/platform/api-reference/projects/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `workspace_id` | path | `string` | yes |
| `data` | body | `object` | yes |
