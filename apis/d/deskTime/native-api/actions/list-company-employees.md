# List Company Employees with DeskTime

Retrieves company employees from DeskTime for a day or month.

## Endpoint

- **Method:** `GET`
- **Path:** `/employees`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [List Company Employees](https://help.desktime.com/hc/en-us/articles/25495139812637-How-to-get-all-company-employees-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Date in YYYY-MM-DD format. |
| `period` | query | `string` | no | Tracking period. Accepted values: `0`, `1`. |
