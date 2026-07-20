# Create Batch with Groq

Creates a batch in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/batches`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Batch](https://console.groq.com/docs/api-reference#batches-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input_file_id` | body | `string` | yes |
| `endpoint` | body | `list` | yes |
| `completion_window` | body | `list` | yes |
| `metadata` | body | `object` | no |
