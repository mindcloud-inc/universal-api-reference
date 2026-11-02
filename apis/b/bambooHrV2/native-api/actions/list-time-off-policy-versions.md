# List Time Off Policy Versions with BambooHR

Lists time off policy versions from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/policies/:id/versions`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Off Policy Versions](https://documentation.bamboohr.com/reference/list-time-off-policy-versions)

## Requirements

- **OAuth scopes:** `time_off:policies`
- **scope:** `time_off:policies` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The time off policy ID. |
| `filter` | query | `string` | no | OData filter expression applied to the policy's versions. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `versionId` (matches the version `id`), `effectiveDate`, `status`. Examples: `status eq 'ARCHIVED'`, `effectiveDate ge '2026-01-01'`, `versionId in (10, 11)`. Note that a version with no effective date stores a zero date rather than NULL, so `effectiveDate eq null` never matches. |
