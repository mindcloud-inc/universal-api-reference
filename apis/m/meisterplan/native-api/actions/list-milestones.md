# List Milestones with Meisterplan

Retrieves a list of milestones from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/milestones`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [List Milestones](https://api.us.meisterplan.com/docs/api.html#operation/GetAllMilestones)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
