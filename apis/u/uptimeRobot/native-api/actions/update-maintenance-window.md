# Update Maintenance Window with UptimeRobot

Updates an existing maintenance window in UptimeRobot.

## Endpoint

- **Method:** `POST`
- **Path:** `/editMWindow`
- **Base URL:** `https://api.uptimerobot.com/v2`
- **Official documentation:** [Update Maintenance Window](https://uptimerobot.com/api/legacy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | ID of the maintenance window to update. |
| `value` | body | `string` | no | Optional recurrence value for weekly or monthly windows, such as 2-4-5. |
| `friendly_name` | body | `string` | yes | Maintenance window display name. |
| `type` | body | `number` | yes | Maintenance window type. Legacy docs: 1 once, 2 daily, 3 weekly, 4 monthly. |
| `start_time` | body | `string` | yes | Start time. Use Unix time for once windows or HH:mm for repeating windows. |
| `duration` | body | `number` | yes | Duration in minutes. |
