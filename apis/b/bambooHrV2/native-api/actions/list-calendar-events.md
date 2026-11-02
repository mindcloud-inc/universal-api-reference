# List Calendar Events with BambooHR

Lists calendar events from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/calendar-events`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Calendar Events](https://documentation.bamboohr.com/reference/list-calendar-events)

## Requirements

- **OAuth scopes:** `calendar:events`
- **scope:** `calendar:events` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | yes | Inclusive start date (YYYY-MM-DD). Interpreted in the company timezone. Format: `YYYY-MM-DD`. |
| `end` | query | `date` | yes | Inclusive end date (YYYY-MM-DD). Must be on or after start; the range must span less than one year. Format: `YYYY-MM-DD`. |
| `filter` | query | `string` | no | OData filter expression applied to calendar events. Supported operators: `eq` (equals), `in` (value in list), `and` (combine clauses). Filterable fields: `type` (one of `TIME_OFF`, `HOLIDAY`, `BIRTHDAY`, `ANNIVERSARY`), `employeeId` (int), `department` (int), `division` (int), `location` (int). Per-employee filters have no effect on HOLIDAY events. Example: `type in ('TIME_OFF','HOLIDAY') and department in (10,20)`. |
| `directReportsOnly` | query | `boolean` | no | When true, restrict employee-bound events to the caller's direct reports. HOLIDAY events are unaffected. Callers with no direct reports receive an empty result for employee-bound types. |
| `includePersons` | query | `boolean` | no | When true, embed a persons map (keyed by employee id) alongside the events. |
