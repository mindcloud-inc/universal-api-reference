# Update Project Estimate with Clockify

Updates a project estimate in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/projects/:projectId/estimate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project Estimate](https://docs.developer.clockify.me/#tag/Project/operation/updateEstimate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `budgetEstimate` | body | `object` | no |
| `estimateReset` | body | `object` | no |
| `timeEstimate` | body | `object` | no |
| `budgetEstimate.active` | body | `boolean` | no |
| `budgetEstimate.estimate` | body | `number` | no |
| `budgetEstimate.includeExpenses` | body | `boolean` | no |
| `budgetEstimate.resetOption` | body | `string` | no |
| `budgetEstimate.type` | body | `string` | no |
| `estimateReset.active` | body | `boolean` | no |
| `estimateReset.dayOfMonth` | body | `number` | no |
| `estimateReset.dayOfWeek` | body | `string` | no |
| `estimateReset.hour` | body | `number` | no |
| `estimateReset.interval` | body | `string` | no |
| `estimateReset.isActive` | body | `boolean` | no |
| `estimateReset.month` | body | `string` | no |
| `timeEstimate.active` | body | `boolean` | no |
| `timeEstimate.estimate` | body | `string` | no |
| `timeEstimate.includeNonBillable` | body | `boolean` | no |
| `timeEstimate.resetOption` | body | `string` | no |
| `timeEstimate.type` | body | `string` | no |
