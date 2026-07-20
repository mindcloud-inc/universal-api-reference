# Create Schedule with Devin

Creates a new schedule in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/schedules`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Create Schedule](https://docs.devin.ai/api-reference/v3/schedules/post-organizations-schedules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | body | `string` | no | Agent type: devin, data_analyst, or advanced. |
| `bypass_approval` | body | `boolean` | no | Whether to bypass approval for scheduled sessions. |
| `frequency` | body | `string` | no | Cron expression for recurring schedules. |
| `name` | body | `string` | yes | Schedule name. |
| `notify_on` | body | `string` | no | Notification policy: always, failure, or never. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `prompt` | body | `string` | yes | Prompt to run for scheduled sessions. |
| `schedule_type` | body | `string` | no | Schedule type: recurring or one_time. |
| `scheduled_at` | body | `date` | no | ISO 8601 datetime for one-time schedules. |
