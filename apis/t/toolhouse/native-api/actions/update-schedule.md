# Update Schedule with Toolhouse

## Endpoint

- **Method:** `PUT`
- **Path:** `/schedules/:schedule_id`
- **Base URL:** `https://api.toolhouse.ai/v1`
- **Official documentation:** [Update Schedule](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the schedule should remain active. |
| `bundle` | body | `string` | no | Optional Toolhouse bundle name. |
| `cadence` | body | `string` | yes | The cron cadence for the autonomous run. |
| `callback_url` | body | `string` | no | Optional webhook URL to receive schedule callbacks. |
| `chat_id` | body | `string` | no | Optional Toolhouse chat ID to re-target the schedule. |
| `schedule_id` | path | `string` | yes | The Toolhouse schedule ID. |
| `toolhouse_id` | body | `string` | no | Optional Toolhouse workspace identifier. |
| `vars` | body | `object` | no | Variables passed to scheduled runs. |
