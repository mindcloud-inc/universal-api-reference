# Update Public Status Page with UptimeRobot

Updates an existing public status page in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/editPSP`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Update Public Status Page](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | ID of the status page to update. |
| `type` | body | `number` | yes | Status page type. Legacy docs examples use 1. |
| `friendly_name` | body | `string` | yes | Status page display name. |
| `monitors` | body | `string` | yes | Dash-separated monitor IDs to display, or 0 for all monitors. |
