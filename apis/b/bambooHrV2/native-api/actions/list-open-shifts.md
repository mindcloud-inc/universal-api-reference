# List Open Shifts with BambooHR

Lists open shifts from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/open-shifts`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Open Shifts](https://documentation.bamboohr.com/reference/scheduling-list-open-shifts)

## Requirements

- **OAuth scopes:** `scheduling:shifts`
- **scope:** `scheduling:shifts` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | OData v4 filter expression. Required: a date window on start or end, bounded below (ge, gt, eq) and above (le, lt, eq), at most 31 days wide. Allowed fields: id, scheduleId, name, start, end, claimsRequireApproval. |
| `sort` | query | `string` | no | Sort expression on any filterable field (e.g. start desc). Defaults to start ascending. |
