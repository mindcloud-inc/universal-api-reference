# Get Compensation Planning Approval Flows with BambooHR

Retrieves compensation planning approval flows from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/planning_cycles/:id/approvals`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Planning Approval Flows](https://documentation.bamboohr.com/reference/552aef08bdce5fca9ed705bfdcb945b5)

## Requirements

- **OAuth scopes:** `planning_cycles`
- **scope:** `planning_cycles` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `groupBy` | query | `string` | no | Optional grouping for flows (e.g. department) |
