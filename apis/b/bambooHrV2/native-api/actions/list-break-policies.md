# List Break Policies with BambooHR

Lists break policies from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/break-policies`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Break Policies](https://documentation.bamboohr.com/reference/list-break-policies)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to break policies. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `name`, `description`, `allEmployeesAssigned`, `createdAt`, `updatedAt`, `deletedAt`. Examples: `name eq 'Standard Lunch'`, `description eq null`, `allEmployeesAssigned eq true and name ne 'Legacy'`. |
| `includeCounts` | query | `boolean` | no | Include employee and break counts |
