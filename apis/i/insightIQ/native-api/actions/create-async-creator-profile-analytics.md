# Create Async Creator Profile Analytics with InsightIQ

Creates an async creator analytics request in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/social/creators/async/profiles/analytics`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Async Creator Profile Analytics](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | URL, username, handle, or profile URL to analyze |
| `is_premium` | body | `boolean` | no | Premium analytics mode for Twitch only |
| `metric_calculation_method` | body | `string` | no | Metric aggregation method; supports average or median |
| `work_platform_id` | body | `string` | yes | Work platform ID for the profile lookup |
