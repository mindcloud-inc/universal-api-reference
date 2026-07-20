# Get Project Totals with Clockify

Retrieves project totals for one project from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/projects/totals/:projectId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Project Totals](https://docs.developer.clockify.me/#tag/Scheduling/operation/getProjectTotalsForSingleProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | query | `string` | yes |
| `projectId` | path | `string` | yes |
| `start` | query | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |
