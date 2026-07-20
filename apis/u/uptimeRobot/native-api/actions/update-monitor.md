# Update Monitor with UptimeRobot

Updates an existing monitor in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/editMonitor`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Update Monitor](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `friendly_name` | body | `string` | no | Optional new display name. |
| `id` | body | `number` | yes | ID of the monitor to update. |
| `status` | body | `number` | no | Optional monitor state. Legacy docs: 0 pause, 1 resume. |
