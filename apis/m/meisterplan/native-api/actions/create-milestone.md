# Create Milestone with Meisterplan

Creates a new milestone in Meisterplan.

## Endpoint

- **Method:** `POST`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/milestones`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Create Milestone](https://api.us.meisterplan.com/docs/api.html#operation/CreateMilestone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `name` | body | `string` | yes | Milestone name. |
| `date` | body | `string` | yes | Milestone date in YYYY-MM-DD format. |
