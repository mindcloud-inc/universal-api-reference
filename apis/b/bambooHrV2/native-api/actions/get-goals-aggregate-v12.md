# Get Goals Aggregate V1 2 with BambooHR

Retrieves goals aggregate v1 2 from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1_2/performance/employees/:employeeId/goals/aggregate`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Goals Aggregate V1 2](https://documentation.bamboohr.com/reference/get-goals-aggregate-v1_2)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee whose goals are aggregated. |
| `filter` | query | `string` | no | Optional status filter for the goals collection in the aggregate response. Use `status-all` for a full dashboard across statuses; otherwise pass `status-inProgress`, `status-completed`, or `status-closed`. If omitted or invalid, defaults to the first available filter. The response's `filters` counts may include statuses beyond the selected goal list. |
