# Get Employee Projects with DeskTime

Retrieves an employee's tracked projects from DeskTime for a date.

## Endpoint

- **Method:** `GET`
- **Path:** `/employee/projects`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [Get Employee Projects](https://help.desktime.com/hc/en-us/articles/25494912262301-How-to-get-employee-projects-data-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Employee ID. |
| `date` | query | `string` | no | Date in YYYY-MM-DD format. |
