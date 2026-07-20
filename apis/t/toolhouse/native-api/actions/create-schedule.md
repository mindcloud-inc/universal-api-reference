# Create Schedule with Toolhouse

## Endpoint

- **Method:** `POST`
- **Path:** `/schedules`
- **Base URL:** `https://api.toolhouse.ai/v1`
- **Official documentation:** [Create Schedule](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundle` | body | `string` | no | Optional Toolhouse bundle name. |
| `cadence` | body | `string` | yes | The cron cadence for the autonomous run. |
| `callback_url` | body | `string` | no | Optional webhook URL to receive schedule callbacks. |
| `chat_id` | body | `string` | yes | The Toolhouse chat ID to schedule. |
| `toolhouse_id` | body | `string` | no | Optional Toolhouse workspace identifier. |
| `vars` | body | `object` | no | Variables passed to scheduled runs. |
