# Get Goal Filters V1 2 with BambooHR

Retrieves goal filters v1 2 from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1_2/performance/employees/:employeeId/goals/filters`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Goal Filters V1 2](https://documentation.bamboohr.com/reference/get-goals-filters-v1_2)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee the goals are assigned to. |
