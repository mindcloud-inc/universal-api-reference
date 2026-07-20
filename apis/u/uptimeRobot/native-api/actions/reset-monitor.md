# Reset Monitor with UptimeRobot

Resets an existing monitor's stats and response times in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/resetMonitor`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Reset Monitor](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | ID of the monitor to reset. |
