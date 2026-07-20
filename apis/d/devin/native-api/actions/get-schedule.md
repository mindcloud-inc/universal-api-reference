# Get Schedule with Devin

Retrieves a schedule record from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/schedules/:schedule_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Get Schedule](https://docs.devin.ai/api-reference/v3/schedules/get-organizations-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `schedule_id` | path | `string` | yes | Scheduled session ID. |
