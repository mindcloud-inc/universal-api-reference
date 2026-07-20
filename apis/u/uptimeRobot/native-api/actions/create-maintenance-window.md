# Create Maintenance Window with UptimeRobot

Creates a new maintenance window in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/newMWindow`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Create Maintenance Window](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `friendly_name` | body | `string` | yes | Maintenance window display name. |
| `value` | body | `string` | no | Optional recurrence value for weekly or monthly windows, such as 2-4-5. |
| `type` | body | `number` | yes | Maintenance window type. Legacy docs: 1 once, 2 daily, 3 weekly, 4 monthly. |
| `start_time` | body | `string` | yes | Start time. Use Unix time for once windows or HH:mm for repeating windows. |
| `duration` | body | `number` | yes | Duration in minutes. |
