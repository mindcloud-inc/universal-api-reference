# List Goal Comments with BambooHR

Lists goal comments from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/performance/employees/:employeeId/goals/:goalId/comments`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Goal Comments](https://documentation.bamboohr.com/reference/list-goal-comments)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee the goal is associated with. |
| `goalId` | path | `string` | yes | goalId is the goal ID for the specified employee. |
