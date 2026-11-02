# Get Compensation Planning Worksheet CSV with BambooHR

Retrieves compensation planning worksheet csv from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id/worksheet/export`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Planning Worksheet CSV](https://documentation.bamboohr.com/reference/f4ccbeaf25b2344e5026de3c8189dd5e)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — Required OAuth scope documented by BambooHR.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `type` | query | `list<string>` | no | Worksheet context: recommendations, approvals, or overview (overview requires cycle admin). Accepted values: `approvals`, `overview`, `recommendations`. |
