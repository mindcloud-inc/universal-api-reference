# List Company Holidays with BambooHR

Lists company holidays from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/holidays`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Company Holidays](https://documentation.bamboohr.com/reference/list-company-holidays)

## Requirements

- **OAuth scopes:** `holidays`
- **scope:** `holidays` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to company holidays. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `name`, `startDate`, `endDate`, `isPublic`, `globalHolidayUuid`. Examples: `startDate ge '2026-01-01'`, `isPublic eq true and endDate ne null`. |
| `orderBy` | query | `string` | no | Comma-separated list of sort terms, each a field optionally followed by `asc` or `desc`. Allowed sort fields: `name`, `startDate`, `endDate`, `createdAt`, `updatedAt`. Send multiple values as a string separated by `,`. |
| `select` | query | `string` | no | Comma-separated list of properties to include in each returned holiday. Reduces payload size. Example: `id,name,startDate`. Send multiple values as a string separated by `,`. |
