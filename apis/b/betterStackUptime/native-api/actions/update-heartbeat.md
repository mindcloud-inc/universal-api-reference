# Update Heartbeat with Better Stack Uptime

Updates an existing heartbeat in Better Stack Uptime.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/heartbeats/:heartbeat_id`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Update Heartbeat](https://betterstack.com/docs/uptime/api/update-existing-hearbeat/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `heartbeat_id` | path | `string` | yes | The heartbeat ID. |
| `name` | body | `string` | no | The heartbeat name. |
| `period` | body | `number` | no | The expected heartbeat period in seconds. |
| `grace` | body | `number` | no | The grace period in seconds. |
| `email` | body | `boolean` | no | Whether email alerts are enabled. |
| `sms` | body | `boolean` | no | Whether SMS alerts are enabled. |
| `call` | body | `boolean` | no | Whether call alerts are enabled. |
| `push` | body | `boolean` | no | Whether push alerts are enabled. |
| `critical_alert` | body | `boolean` | no | Whether critical alerts are enabled. |
| `team_wait` | body | `boolean` | no | Whether team wait is enabled. |
| `paused` | body | `boolean` | no | Whether the heartbeat is paused. |
| `sort_index` | body | `number` | no | The sort index. |
| `maintenance_days[]` | body | `array<string>` | no | Maintenance days. |
| `maintenance_from` | body | `string` | no | Maintenance window start time. |
| `maintenance_to` | body | `string` | no | Maintenance window end time. |
| `maintenance_timezone` | body | `string` | no | Maintenance timezone. |
| `heartbeat_group_id` | body | `number` | no | The heartbeat group ID. |
| `policy_id` | body | `number` | no | The escalation policy ID. |
