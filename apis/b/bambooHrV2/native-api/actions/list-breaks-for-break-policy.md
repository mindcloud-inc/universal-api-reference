# List Breaks for Break Policy with BambooHR

Lists breaks for break policy from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/break-policies/:id/breaks`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Breaks for Break Policy](https://documentation.bamboohr.com/reference/list-break-policy-breaks)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The break policy ID. |
| `filter` | query | `string` | no | OData filter expression applied to breaks within the policy. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `name`, `paid`, `duration`, `availabilityType`, `availabilityMinHoursWorked`, `availabilityMaxHoursWorked`, `availabilityStartTime`, `availabilityEndTime`, `createdAt`, `updatedAt`, `deletedAt`. Examples: `name eq 'Lunch'`, `paid eq true`, `paid eq false and name ne 'Quick Break'`. |
