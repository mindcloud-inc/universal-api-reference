# List Hour Entries with BambooHR

Lists hour entries from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/hour-entries`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Hour Entries](https://documentation.bamboohr.com/reference/list-hour-entries)

## Requirements

- **OAuth scopes:** `time_tracking:timesheets`
- **scope:** `time_tracking:timesheets` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Supported operators: `eq`, `ge`, `le`, `and`. Filterable fields: `timesheetId`, `employeeId`, `date`. Examples: `employeeId eq 40342`, `date ge 2025-01-01 and date le 2025-01-31`, `timesheetId eq 9001`. |
| `sort` | query | `string` | no | Sort expression like `date desc` or `updatedAt asc`. Allowed fields: `date`, `updatedAt`. Defaults to `date desc`. |
