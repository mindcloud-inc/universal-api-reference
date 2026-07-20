# List Projects with Frame.io v4

Retrieves projects from a workspace in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/workspaces/:workspaceId/projects`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Projects](https://next.developer.frame.io/platform/api-reference/projects/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `workspace_id` | path | `string` | yes |
| `include` | query | `string` | no |
