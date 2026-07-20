# Get Platform Analytics with Ringg AI

Retrieves platform analytics from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/platform-analytics`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Platform Analytics](https://docs.ringg.ai/api-reference/endpoint/analytics/get-platform-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start date for analytics filter (YYYY-MM-DD format) |
| `end_date` | query | `string` | no | End date for analytics filter (YYYY-MM-DD format) |
| `agent_id` | query | `string` | no | Filter by specific agent ID |
| `bulk_list_id` | query | `string` | no | Filter by specific bulk list/campaign ID |
| `voicemail` | query | `boolean` | no | Filter by voicemail status |
