# Get Goal Creation Permission with BambooHR

Retrieves goal creation permission from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/performance/employees/:employeeId/goals/canCreateGoals`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Goal Creation Permission](https://documentation.bamboohr.com/reference/get-goal-creation-permission)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee whose goal creation permission is returned. |
