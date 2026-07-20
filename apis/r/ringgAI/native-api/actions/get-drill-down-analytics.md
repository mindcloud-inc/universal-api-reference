# Get Drill-Down Analytics with Ringg AI

Retrieves drill-down analytics from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/drill-down-analytics`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Drill-Down Analytics](https://docs.ringg.ai/api-reference/endpoint/analytics/get-drill-down-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulk_list_id` | query | `string` | yes | (Required) Bulk list/campaign ID to get drill-down analytics for |
| `start_date` | query | `string` | no | Start date for analytics filter (YYYY-MM-DD format) |
| `end_date` | query | `string` | no | End date for analytics filter (YYYY-MM-DD format) |
| `agent_id` | query | `string` | no | Filter by specific agent ID |
| `voicemail` | query | `boolean` | no | Filter by voicemail status |
