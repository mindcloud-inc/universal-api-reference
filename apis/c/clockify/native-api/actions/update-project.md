# Update Project with Clockify

Updates an existing project in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/projects/:projectId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project](https://docs.developer.clockify.me/#tag/Project/operation/updateProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `costRate.amount` | body | `number` | no |
| `costRate.since` | body | `date` | no |
| `hourlyRate.amount` | body | `number` | no |
| `hourlyRate.since` | body | `date` | no |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string` | yes |
| `archived` | body | `boolean` | no |
| `billable` | body | `boolean` | no |
| `clientId` | body | `string` | no |
| `color` | body | `string` | no |
| `costRate` | body | `object` | no |
| `hourlyRate` | body | `object` | no |
| `isPublic` | body | `boolean` | no |
| `name` | body | `string` | no |
| `note` | body | `string` | no |
