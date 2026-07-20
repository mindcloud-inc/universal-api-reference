# Get Call History with Ringg AI

Retrieves call history from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/calling/history`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Call History](https://docs.ringg.ai/api-reference/endpoint/history/get-call-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | no | Filter calls starting from this date (ISO 8601 format with timezone). |
| `end_date` | query | `date` | no | Filter calls up to this date (ISO 8601 format with timezone). |
| `agent_id` | query | `string` | no | Filter calls by assistant ID. |
| `status` | query | `string` | no | Filter calls by status. |
| `bulk_list_id` | query | `string` | no | Filter calls by bulk list ID. |
