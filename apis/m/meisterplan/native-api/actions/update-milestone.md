# Update Milestone with Meisterplan

Updates an existing milestone in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Milestone](https://api.us.meisterplan.com/docs/api.html#operation/UpdateMilestone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `milestoneId` | path | `string` | yes | Internal Meisterplan milestone identifier. |
| `name` | body | `string` | no | Updated milestone name. |
| `date` | body | `string` | no | Updated milestone date in YYYY-MM-DD format. |
