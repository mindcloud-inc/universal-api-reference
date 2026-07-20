# Convert Text to Cron with Toolhouse

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules/text-to-cron`
- **Base URL:** `https://api.toolhouse.ai/v1`
- **Official documentation:** [Convert Text to Cron](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cron` | query | `string` | yes | A natural-language scheduling prompt to convert into cron. |
