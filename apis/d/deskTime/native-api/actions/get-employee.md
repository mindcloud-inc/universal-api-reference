# Get Employee with DeskTime

Retrieves employee tracking data from DeskTime for a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/employee`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [Get Employee](https://help.desktime.com/hc/en-us/articles/25494877861789-How-to-get-employee-data-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Employee ID. |
| `date` | query | `string` | no | Date in YYYY-MM-DD format. |
