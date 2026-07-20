# List Calls with CallScaler

Retrieves calls from CallScaler.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [List Calls](https://callscaler.com/docs/api-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ai_category` | query | `string` | no |
| `call_flow_id` | query | `string` | no |
| `caller_name` | query | `string` | no |
| `direction` | query | `string` | no |
| `end_date` | query | `date` | no |
| `has_transcription` | query | `boolean` | no |
| `include` | query | `string` | no |
| `keyword` | query | `string` | no |
| `max_ai_score` | query | `number` | no |
| `max_duration` | query | `number` | no |
| `min_ai_score` | query | `number` | no |
| `min_duration` | query | `number` | no |
| `number_group_id` | query | `string` | no |
| `number_id` | query | `string` | no |
| `qualified` | query | `boolean` | no |
| `search` | query | `string` | no |
| `source` | query | `string` | no |
| `start_date` | query | `date` | no |
| `status` | query | `string` | no |
| `updated_since` | query | `date` | no |
