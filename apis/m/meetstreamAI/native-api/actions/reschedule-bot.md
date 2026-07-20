# Reschedule Bot with Meetstream AI

Updates a scheduled bot in Meetstream AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/calendar/scheduled_bots/:bot_id`
- **Base URL:** `https://api.meetstream.ai/api/v1`
- **Official documentation:** [Reschedule Bot](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/reschedule-bot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `string` | yes | The scheduled bot identifier. |
| `scheduled_join_time` | body | `date` | yes | The new scheduled join time in ISO 8601 format. |
