# Create Monitor with UptimeRobot

Creates a new monitor in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/newMonitor`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Create Monitor](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `friendly_name` | body | `string` | yes | Monitor display name. |
| `url` | body | `string` | yes | Target URL or IP to monitor. |
| `type` | body | `number` | yes | Monitor type. Legacy docs: 1 HTTP(s), 2 keyword, 3 ping, 4 port, 5 heartbeat. |
| `interval` | body | `number` | no | Optional monitor interval in seconds. |
| `timeout` | body | `number` | no | Optional timeout in seconds for HTTP, keyword, and port monitors. |
