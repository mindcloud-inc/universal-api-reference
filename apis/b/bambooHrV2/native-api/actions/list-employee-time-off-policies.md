# List Employee Time Off Policies with BambooHR

Lists employee time off policies from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:employeeId/time-off/policies`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Time Off Policies](https://documentation.bamboohr.com/reference/list-employee-time-off-policies)

## Requirements

- **OAuth scopes:** `time_off:policies`
- **scope:** `time_off:policies` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `number` | yes | The employee ID. |
| `filter` | query | `string` | no | OData filter expression applied to the employee's policy assignments. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `policyId`, `categoryId`. Examples: `policyId eq 15`, `categoryId in (62, 64)`, `categoryId eq 64 and policyId eq 15`. |
