# Update Schedule with Devin

Updates an existing schedule in Devin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/organizations/:org_id/schedules/:schedule_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Update Schedule](https://docs.devin.ai/api-reference/v3/schedules/patch-organizations-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | no | Whether the schedule is enabled. |
| `frequency` | body | `string` | no | Cron expression for recurring schedules. |
| `name` | body | `string` | no | Schedule name. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `prompt` | body | `string` | no | Prompt to run for scheduled sessions. |
| `schedule_id` | path | `string` | yes | Scheduled session ID. |
| `scheduled_at` | body | `string` | no | ISO 8601 datetime for one-time schedules. |
