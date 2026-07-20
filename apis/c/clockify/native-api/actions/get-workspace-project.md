# Get Workspace Project with Clockify

Retrieves a specific workspace project from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/projects/:projectId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Workspace Project](https://docs.developer.clockify.me/#tag/Project/operation/getProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier. |
| `projectId` | path | `string` | yes | Project identifier. |
| `hydrated` | query | `boolean` | no | Include hydrated project data. |
| `custom-field-entity-type` | query | `string` | no | Custom field entity type filter. |
| `expense-limit` | query | `number` | no | Maximum expenses to include. |
| `expense-date` | query | `string` | no | Include expenses before this date (yyyy-MM-dd). |
