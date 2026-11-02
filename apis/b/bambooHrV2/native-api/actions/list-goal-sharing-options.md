# List Goal Sharing Options with BambooHR

Lists goal sharing options from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/performance/employees/:employeeId/goals/shareOptions`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Goal Sharing Options](https://documentation.bamboohr.com/reference/list-goal-share-options)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee whose goal sharing options are returned. |
| `search` | query | `string` | yes | The search term used to filter employees returned. Will search name, internal employee ID, and email. |
