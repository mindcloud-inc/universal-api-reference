# Get Compensation Planning Cycle Budgets with BambooHR

Retrieves compensation planning cycle budgets from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id/budgets`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Planning Cycle Budgets](https://documentation.bamboohr.com/reference/bdb215e3f9e84ed281eb797b48cc66cc)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
