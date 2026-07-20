# Get Employee Apps with DeskTime

Retrieves an employee's tracked apps from DeskTime for a date.

## Endpoint

- **Method:** `GET`
- **Path:** `/employee/apps`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [Get Employee Apps](https://help.desktime.com/hc/en-us/articles/25494932087709-How-to-get-employee-apps-data-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Employee ID. |
| `date` | query | `string` | no | Date in YYYY-MM-DD format. |
