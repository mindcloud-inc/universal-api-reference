# Get Alignable Goal Options with BambooHR

Retrieves alignable goal options from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/performance/employees/:employeeId/goals/alignmentOptions`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Alignable Goal Options](https://documentation.bamboohr.com/reference/get-alignable-goal-options)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee whose alignable goal options are returned. |
| `goalId` | query | `number` | no | Optional goal ID whose current alignment should be included in the results. Only pass a goal ID that belongs to the specified employee. If this endpoint returns 403 for an otherwise visible goal, report that alignment options are restricted by permissions rather than treating the goal ID as invalid. |
