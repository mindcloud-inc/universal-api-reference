# Get Duration Distribution with Ringg AI

Retrieves duration distribution analytics from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/duration-distribution`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Duration Distribution](https://docs.ringg.ai/api-reference/endpoint/analytics/get-duration-distribution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start date for analytics filter (YYYY-MM-DD format) |
| `end_date` | query | `string` | no | End date for analytics filter (YYYY-MM-DD format) |
| `agent_id` | query | `string` | no | Filter by specific agent ID |
| `bulk_list_id` | query | `string` | no | Filter by specific bulk list/campaign ID |
| `voicemail` | query | `boolean` | no | Filter by voicemail status |
