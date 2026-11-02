# Get Compensation Planning Cycle Worksheet with BambooHR

Retrieves compensation planning cycle worksheet from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id/worksheet`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Planning Cycle Worksheet](https://documentation.bamboohr.com/reference/fdffbb9803f77a9bd0c13a3f206a41d4)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `type` | query | `list<string>` | no | Worksheet context: recommendations, approvals, or overview (overview requires cycle admin). Accepted values: `approvals`, `overview`, `recommendations`. |
