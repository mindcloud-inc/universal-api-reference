# Create Batch with Bland AI

Creates a new call batch in Bland AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/batches/create`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [Create Batch](https://docs.bland.ai/api-v1/post/batches)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `call_objects[]` | body | `array<string>` | no |
| `global` | body | `object` | yes |
| `status_webhook` | body | `string` | no |
