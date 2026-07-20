# Get Workspace User Capacity Total with Clockify

Retrieves a workspace user capacity total from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/users/:userId/totals`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Workspace User Capacity Total](https://docs.developer.clockify.me/#tag/Scheduling/operation/getUserTotalsForSingleUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | query | `string` | yes |
| `page` | query | `number` | no |
| `page-size` | query | `number` | no |
| `start` | query | `string` | yes |
| `userId` | path | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |
