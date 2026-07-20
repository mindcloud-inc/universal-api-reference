# Get Classification Analytics with Ringg AI

Retrieves classification analytics from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/classification-analytics`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Classification Analytics](https://docs.ringg.ai/api-reference/endpoint/analytics/get-classification-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start date for analytics filter (YYYY-MM-DD format) |
| `end_date` | query | `string` | no | End date for analytics filter (YYYY-MM-DD format) |
| `agent_id` | query | `string` | no | Filter by specific agent ID |
| `bulk_list_id` | query | `string` | no | Filter by specific bulk list/campaign ID |
| `voicemail` | query | `boolean` | no | Filter by voicemail status |
