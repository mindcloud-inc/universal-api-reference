# Get Stats with Octanist

Retrieves dashboard statistics from Octanist.

## Endpoint

- **Method:** `POST`
- **Path:** `/stats`
- **Base URL:** `https://octanist.com/api`
- **Official documentation:** [Get Stats](https://octanist.com/docs/api-reference/endpoint/stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | body | `string` | no | Time period to query: current, previous, or custom. |
| `startDate` | body | `string` | no | Start date in YYYY-MM-DD format when period is custom. |
| `endDate` | body | `string` | no | End date in YYYY-MM-DD format when period is custom. |
