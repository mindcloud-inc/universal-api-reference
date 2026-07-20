# Get Public Status Pages with UptimeRobot

Retrieves public status pages from UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/getPSPs`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Get Public Status Pages](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `psps` | body | `string` | no | Optional dash-separated public status page IDs to filter. |
| `offset` | body | `number` | no | Pagination offset. |
| `limit` | body | `number` | no | Pagination limit, max 50. |
