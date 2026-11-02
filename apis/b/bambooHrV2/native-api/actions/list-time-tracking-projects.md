# List Time Tracking Projects with BambooHR

Lists time tracking projects from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/projects`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Projects](https://documentation.bamboohr.com/reference/list-projects)

## Requirements

- **OAuth scopes:** `time_tracking:project`
- **scope:** `time_tracking:project` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `id`, `name`, `billable`, `includeInPayroll`, `allEmployeesAssigned`, `archived`, `createdAt`, `updatedAt`. |
| `sort` | query | `string` | no | Sort expression like `name asc, createdAt desc`. Allowed fields: `name`, `createdAt`, `updatedAt`. |
