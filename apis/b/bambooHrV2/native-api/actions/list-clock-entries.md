# List Clock Entries with BambooHR

Lists clock entries from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/clock-entries`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Clock Entries](https://documentation.bamboohr.com/reference/list-clock-entries)

## Requirements

- **OAuth scopes:** `time_tracking:timesheets`
- **scope:** `time_tracking:timesheets` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Supported operators: `eq`, `ge`, `le`, `and`. Filterable fields: `timesheetId`, `employeeId`, `start`, `end`. Examples: `employeeId eq 40342`, `start ge 2026-03-16T00:00:00Z and start le 2026-03-29T23:59:59Z`, `timesheetId eq 9001`. |
| `sort` | query | `string` | no | Sort expression like `start desc` or `updatedAt asc`. Allowed fields: `start`, `end`, `updatedAt`. Defaults to `start desc`. |
