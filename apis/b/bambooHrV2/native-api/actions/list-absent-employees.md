# List Absent Employees with BambooHR

Lists absent employees from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/whos-out`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Absent Employees](https://documentation.bamboohr.com/reference/list-whos-out-v1)

## Requirements

- **OAuth scopes:** `time_off`
- **scope:** `time_off` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | yes | Inclusive start date (YYYY-MM-DD). Interpreted in the company timezone. Format: `YYYY-MM-DD`. |
| `end` | query | `date` | yes | Inclusive end date (YYYY-MM-DD). Must be on or after start; the range may not exceed 366 days. Format: `YYYY-MM-DD`. |
| `filter` | query | `string` | no | OData filter expression applied to who's out results. Supported operators: `eq` (equals), `in` (value in list), `and` (combine clauses). Filterable fields: `employeeId` (int), `department` (int), `division` (int), `location` (int). Examples: `employeeId eq 42`, `department in (10, 20) and location eq 5`. |
| `directReportsOnly` | query | `boolean` | no | When true, restrict to time off for the caller's direct reports. Callers with no direct reports receive an empty result. |
| `includePersons` | query | `boolean` | no | When true, embed a persons map of employee display data alongside results. |
