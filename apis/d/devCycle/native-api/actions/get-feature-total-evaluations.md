# Get Feature Total Evaluations with DevCycle

Retrieves total feature evaluations from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/results/total-evaluations`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Feature Total Evaluations](https://docs.devcycle.com/management-api/#tag/Results/operation/ResultsController_getTotalEvaluationsPerHourByFeature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Inclusive ISO-8601 end timestamp. |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
| `startDate` | query | `string` | no | Inclusive ISO-8601 start timestamp. |
