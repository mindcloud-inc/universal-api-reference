# Download Call History with Ringg AI

Downloads call history from Ringg AI as CSV.

## Endpoint

- **Method:** `POST`
- **Path:** `/calling/history/download`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Download Call History](https://docs.ringg.ai/api-reference/endpoint/history/download-call-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | no | Filter calls starting from this date (ISO 8601 format with timezone) |
| `end_date` | query | `date` | no | Filter calls up to this date (ISO 8601 format with timezone) |
| `agent_id[]` | query | `array<string>` | no | Filter by agent ID(s) - can be repeated for multiple agents. |
| `status` | query | `string` | no | Filter by call status. |
| `include_analysis` | query | `boolean` | no | Include call analysis data (platform_analysis and client_analysis) in the export. |
| `call_type` | query | `string` | no | Filter by call type. |
| `bulk_list_id` | query | `string` | no | Filter by bulk list ID. |
| `voicemail` | query | `boolean` | no | Filter by voicemail status. |
| `from_number` | query | `string` | no | Filter by caller phone number. |
| `to_number` | query | `string` | no | Filter by callee phone number. |
| `call_id` | query | `string` | no | Filter by specific call ID. |
