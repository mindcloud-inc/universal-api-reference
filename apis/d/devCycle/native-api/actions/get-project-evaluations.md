# Get Project Evaluations with DevCycle

Retrieves project evaluations from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/results/evaluations`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Project Evaluations](https://docs.devcycle.com/management-api/#tag/Results/operation/ResultsController_getEvaluationsPerHourByProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Inclusive ISO-8601 end timestamp. |
| `project` | path | `string` | no | Project key. |
| `startDate` | query | `string` | no | Inclusive ISO-8601 start timestamp. |
