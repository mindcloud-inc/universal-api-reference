# List Break Assessments with BambooHR

Lists break assessments from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/break-assessments`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Break Assessments](https://documentation.bamboohr.com/reference/list-break-assessments)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to break assessments. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `breakId`, `employeeId`, `employeeTimesheetId`, `date`, `result`, `availableYmdt`, `unavailableYmdt`, `expectedDuration`, `recordedDuration`, `durationDifference`, `createdAt`, `updatedAt`. Examples: `employeeId eq 614`, `employeeId in (614, 615, 616)`, `breakId eq 'abc-123' and employeeId eq 614`. |
