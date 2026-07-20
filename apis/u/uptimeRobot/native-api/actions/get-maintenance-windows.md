# Get Maintenance Windows with UptimeRobot

Retrieves maintenance windows and details from UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/getMWindows`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Get Maintenance Windows](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mwindows` | body | `string` | no | Optional dash-separated maintenance window IDs to filter. |
| `offset` | body | `number` | no | Pagination offset. |
| `limit` | body | `number` | no | Pagination limit, max 50. |
