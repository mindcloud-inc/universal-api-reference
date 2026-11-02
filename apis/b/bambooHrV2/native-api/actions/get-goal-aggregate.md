# Get Goal Aggregate with BambooHR

Retrieves goal aggregate from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/performance/employees/:employeeId/goals/:goalId/aggregate`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Goal Aggregate](https://documentation.bamboohr.com/reference/get-goal-aggregate)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee the goal is associated with. |
| `goalId` | path | `string` | yes | goalId is the Goal ID used to generate the aggregate information. |
