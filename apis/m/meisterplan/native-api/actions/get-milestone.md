# Get Milestone with Meisterplan

Retrieves a milestone from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Get Milestone](https://api.us.meisterplan.com/docs/api.html#operation/GetMilestoneById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `milestoneId` | path | `string` | yes | Internal Meisterplan milestone identifier. |
