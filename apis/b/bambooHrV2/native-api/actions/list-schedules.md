# List Schedules with BambooHR

Lists schedules from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/schedules`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Schedules](https://documentation.bamboohr.com/reference/scheduling-list-schedules)

## Requirements

- **OAuth scopes:** `scheduling:schedules time_tracking`
- **scope:** `scheduling:schedules, time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to schedules. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `name`, `locationId`, `timezone`, `startOfWeek`, `earlyClockInThreshold`, `lateClockInThreshold`, `earlyClockOutThreshold`, `lateClockOutThreshold`, `createdAt`, `updatedAt`, `deletedAt`. Examples: `name eq 'Default Schedule'`, `deletedAt eq null`, `name eq 'Default Schedule' and locationId in (1, 2)`. |
| `sort` | query | `string` | no | Sorting options. Supported sorts are: name, locationId, timezone, startOfWeek, earlyClockInThreshold, lateClockInThreshold, earlyClockOutThreshold, lateClockOutThreshold, createdAt, updatedAt, deletedAt |
