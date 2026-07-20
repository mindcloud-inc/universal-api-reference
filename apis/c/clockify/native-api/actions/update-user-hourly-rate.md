# Update User Hourly Rate with Clockify

Updates a user hourly rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/users/:userId/hourly-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update User Hourly Rate](https://docs.developer.clockify.me/#tag/Workspace/operation/setHourlyRateForUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
