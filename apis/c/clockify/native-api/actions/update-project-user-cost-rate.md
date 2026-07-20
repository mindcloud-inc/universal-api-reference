# Update Project User Cost Rate with Clockify

Updates a project user cost rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/projects/:projectId/users/:userId/cost-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project User Cost Rate](https://docs.developer.clockify.me/#tag/Project/operation/addUsersCostRate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
