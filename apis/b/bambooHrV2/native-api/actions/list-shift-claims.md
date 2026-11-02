# List Shift Claims with BambooHR

Lists shift claims from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/shift-claims`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Shift Claims](https://documentation.bamboohr.com/reference/scheduling-list-shift-claims)

## Requirements

- **OAuth scopes:** `scheduling:shifts`
- **scope:** `scheduling:shifts` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Allowed fields: id, shiftId, employeeId, status, resolutionReason, createdAt, updatedAt. |
| `sort` | query | `string` | no | Sort expression on any filterable field (e.g. createdAt desc). Defaults to createdAt ascending. |
