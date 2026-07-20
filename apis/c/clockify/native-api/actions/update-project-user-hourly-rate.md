# Update Project User Hourly Rate with Clockify

Updates a project user hourly rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/projects/:projectId/users/:userId/hourly-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project User Hourly Rate](https://docs.developer.clockify.me/#tag/Project/operation/addUsersHourlyRate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
