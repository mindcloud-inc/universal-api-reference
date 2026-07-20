# Create Project with Clockify

Creates a new project in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/projects`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Project](https://docs.developer.clockify.me/#tag/Project/operation/createNewProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `costRate.amount` | body | `number` | no | — |
| `costRate.since` | body | `date` | no | — |
| `estimate.estimate` | body | `string` | no | — |
| `estimate.type` | body | `list<string>` | no | Accepted values: `AUTO`, `MANUAL`. |
| `hourlyRate.amount` | body | `number` | no | — |
| `hourlyRate.since` | body | `date` | no | — |
| `workspaceId` | path | `list<string>` | yes | — |
| `name` | body | `string` | yes | — |
| `billable` | body | `boolean` | no | — |
| `clientId` | body | `string` | no | — |
| `color` | body | `string` | no | — |
| `costRate` | body | `object` | no | — |
| `estimate` | body | `object` | no | — |
| `hourlyRate` | body | `object` | no | — |
| `isPublic` | body | `boolean` | no | — |
| `note` | body | `string` | no | — |
| `memberships[]` | body | `array<object>` | no | — |
| `tasks[]` | body | `array<object>` | no | — |
