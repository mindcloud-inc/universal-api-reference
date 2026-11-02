# List Scheduling Timezones with BambooHR

Lists scheduling timezones from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/timezones`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Scheduling Timezones](https://documentation.bamboohr.com/reference/scheduling-list-timezones)

## Requirements

- **OAuth scopes:** `scheduling:schedules time_tracking`
- **scope:** `scheduling:schedules, time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to the `name` field. Supported operators: `eq` (exact match), `ne` (exclude), `and` (combine clauses). Supported string functions: `contains`, `startswith`, `endswith` (all case-insensitive). Not supported: `or`, `not`, parenthesized grouping. Examples: `name eq 'America/Denver'`, `name ne 'UTC'`, `contains(name, 'America')`, `startswith(name, 'US/')`, `endswith(name, 'York')`. |
| `sort` | query | `string` | no | Sorting options. Supported sort fields: `name` (alphabetical), `offset` (numeric UTC offset). Example: `name asc` or `offset desc` |
