# Delete Milestone with Meisterplan

Deletes an existing milestone from Meisterplan.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Delete Milestone](https://api.us.meisterplan.com/docs/api.html#operation/DeleteMilestone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `milestoneId` | path | `string` | yes | Internal Meisterplan milestone identifier. |
