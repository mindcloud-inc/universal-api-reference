# Get Change Communication Letter Details with BambooHR

Retrieves change communication letter details from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id/change_comm`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Change Communication Letter Details](https://documentation.bamboohr.com/reference/6c7522fc5664153e97459c2b76ca55ca)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
