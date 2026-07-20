# Update Workspace Cost Rate with Clockify

Updates a workspace cost rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/cost-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Workspace Cost Rate](https://docs.developer.clockify.me/#tag/Workspace/operation/setWorkspaceCostRate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
