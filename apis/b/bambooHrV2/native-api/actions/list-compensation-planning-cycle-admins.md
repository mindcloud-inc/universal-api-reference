# List Compensation Planning Cycle Admins with BambooHR

Lists compensation planning cycle admins from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id/admins`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Compensation Planning Cycle Admins](https://documentation.bamboohr.com/reference/8033792a7b9b696a22d0bd19ff09b1df)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
