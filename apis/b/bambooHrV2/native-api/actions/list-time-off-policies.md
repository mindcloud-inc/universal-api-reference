# List Time Off Policies with BambooHR

Lists time off policies from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/policies`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Off Policies](https://documentation.bamboohr.com/reference/list-time-off-policies-v1)

## Requirements

- **OAuth scopes:** `time_off:policies`
- **scope:** `time_off:policies` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to time off policies. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `name`, `categoryId`, `type`, `createdAt`, `updatedAt`. Examples: `type eq 'ACCRUING'`, `categoryId in (22, 23)`, `type eq 'ACCRUING' and name eq 'Standard Vacation'`. |
| `orderBy` | query | `string` | no | Sort the results by a property and direction, e.g. `name asc`. Sortable fields: `id`, `name`, `categoryId`, `type`, `createdAt`, `updatedAt`. |
