# List Timesheets with BambooHR

Lists timesheets from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/timesheets`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Timesheets](https://documentation.bamboohr.com/reference/list-timesheets)

## Requirements

- **OAuth scopes:** `time_tracking:timesheets`
- **scope:** `time_tracking:timesheets` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData-style filter expression. |
| `sort` | query | `string` | no | Sort expression. Default: startDate desc. |
