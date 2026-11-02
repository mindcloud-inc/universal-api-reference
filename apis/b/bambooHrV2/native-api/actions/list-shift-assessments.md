# List Shift Assessments with BambooHR

Lists shift assessments from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/shift-assessments`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Shift Assessments](https://documentation.bamboohr.com/reference/scheduling-list-shift-assessments)

## Requirements

- **OAuth scopes:** `scheduling:shifts`
- **scope:** `scheduling:shifts` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Must include at least one of: employeeId eq {int}, shiftId eq {uuid}, or a date filter (eq/ge/gt/le/lt on date). Allowed fields: employeeId, shiftId, date. |
| `sort` | query | `string` | no | Sort expression (e.g. date desc). |
