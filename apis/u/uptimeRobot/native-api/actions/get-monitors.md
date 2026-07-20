# Get Monitors with UptimeRobot

Retrieves monitors and monitoring details from UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/getMonitors`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Get Monitors](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitors` | body | `string` | no | Optional dash-separated monitor IDs to filter. |
| `offset` | body | `number` | no | Pagination offset. |
| `limit` | body | `number` | no | Pagination limit, max 50. |
