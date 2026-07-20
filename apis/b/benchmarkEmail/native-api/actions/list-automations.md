# List Automations with Benchmark Email

Retrieves a list of automations from Benchmark Email.

## Endpoint

- **Method:** `GET`
- **Path:** `/Automation/`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [List Automations](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filter` | query | `string` | no | Optional automation name filter. |
| `OrderBy` | query | `string` | no | Automation sort column. |
| `PageNumber` | query | `string` | no | Optional page number for automation results. |
| `PageSize` | query | `string` | no | Number of automation rows to return. |
| `SortOrder` | query | `string` | no | Automation sort direction. |
