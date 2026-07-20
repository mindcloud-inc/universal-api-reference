# Update User Cost Rate with Clockify

Updates a user cost rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/users/:userId/cost-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update User Cost Rate](https://docs.developer.clockify.me/#tag/Workspace/operation/setCostRateForUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
