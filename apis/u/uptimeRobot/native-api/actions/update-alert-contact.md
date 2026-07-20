# Update Alert Contact with UptimeRobot

Updates an existing alert contact in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/editAlertContact`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Update Alert Contact](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | ID of the alert contact to update. |
| `friendly_name` | body | `string` | no | Optional new display name. |
| `value` | body | `string` | no | Optional new destination value. Legacy docs allow this for web-hook contacts. |
