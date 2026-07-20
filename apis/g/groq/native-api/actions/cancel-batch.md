# Cancel Batch with Groq

Cancels a batch in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/batches/:batch_id/cancel`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Cancel Batch](https://console.groq.com/docs/api-reference#batches-cancel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `batch_id` | path | `string` | yes |
