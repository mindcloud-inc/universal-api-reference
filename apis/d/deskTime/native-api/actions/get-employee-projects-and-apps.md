# Get Employee Projects and Apps with DeskTime

Retrieves an employee's tracked projects and apps from DeskTime.

## Endpoint

- **Method:** `GET`
- **Path:** `/employee/basic`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [Get Employee Projects and Apps](https://help.desktime.com/hc/en-us/articles/25494997505053-How-to-get-employee-projects-and-apps-data-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Employee ID. |
| `date` | query | `string` | no | Date in YYYY-MM-DD format. |
