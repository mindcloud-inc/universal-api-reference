# Create Fine Tuning with Groq

Creates a fine-tuning job in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/fine_tunings`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Fine Tuning](https://console.groq.com/docs/api-reference#fine-tuning-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input_file_id` | body | `string` | no |
| `name` | body | `string` | no |
| `type` | body | `string` | no |
| `base_model` | body | `string` | no |
