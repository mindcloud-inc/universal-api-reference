# Get Project Total Evaluations with DevCycle

Retrieves total project evaluations from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/results/total-evaluations`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Project Total Evaluations](https://docs.devcycle.com/management-api/#tag/Results/operation/ResultsController_getTotalEvaluationsPerHourByProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Inclusive ISO-8601 end timestamp. |
| `project` | path | `string` | no | Project key. |
| `startDate` | query | `string` | no | Inclusive ISO-8601 start timestamp. |
