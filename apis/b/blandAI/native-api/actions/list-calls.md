# List Calls with Bland AI

Retrieves calls from your Bland AI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/calls`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [List Calls](https://docs.bland.ai/api-v1/get/calls)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `from_number` | query | `string` | no |
| `to_number` | query | `string` | no |
| `from` | query | `number` | no |
| `to` | query | `number` | no |
| `limit` | query | `number` | no |
| `ascending` | query | `boolean` | no |
| `sort_by` | query | `string` | no |
| `start_date` | query | `string` | no |
| `end_date` | query | `string` | no |
| `created_at` | query | `string` | no |
| `timezone` | query | `string` | no |
| `update_start_date` | query | `string` | no |
| `update_end_date` | query | `string` | no |
| `completed` | query | `boolean` | no |
| `batch_id` | query | `string` | no |
| `answered_by` | query | `string` | no |
| `inbound` | query | `boolean` | no |
| `duration_gt` | query | `number` | no |
| `duration_lt` | query | `number` | no |
| `campaign_id` | query | `string` | no |
