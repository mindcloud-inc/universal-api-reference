# Get Compensation Planning Cycle Details with BambooHR

Retrieves compensation planning cycle details from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Planning Cycle Details](https://documentation.bamboohr.com/reference/342202015a4b67f43d3b993707f544c1)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
