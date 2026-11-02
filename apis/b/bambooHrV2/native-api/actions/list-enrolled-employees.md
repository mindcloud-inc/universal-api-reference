# List Enrolled Employees with BambooHR

Lists enrolled employees from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/employees`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Enrolled Employees](https://documentation.bamboohr.com/reference/list-time-tracking-employees)

## Requirements

- **OAuth scopes:** `time_tracking:employees`
- **scope:** `time_tracking:employees` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `enabled`, `configurationId`. Example: `enabled eq true and configurationId eq 3`. |
| `orderBy` | query | `string` | no | Sort expression like `employeeId asc, createdAt desc`. Allowed fields: `employeeId`, `enabledOn`, `createdAt`, `updatedAt`. |
| `select` | query | `string` | no | Comma-separated list of properties to return (sparse fieldsets). Send multiple values as a string separated by `,`. |
