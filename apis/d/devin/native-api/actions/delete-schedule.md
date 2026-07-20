# Delete Schedule with Devin

Deletes an existing schedule from Devin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/organizations/:org_id/schedules/:schedule_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Delete Schedule](https://docs.devin.ai/api-reference/v3/schedules/delete-organizations-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `schedule_id` | path | `string` | yes | Scheduled session ID. |
