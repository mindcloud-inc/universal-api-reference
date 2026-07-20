# Create Edit with Uwear.ai

Creates an edited generation in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/generation-edit`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Create Edit](https://docs.dev.uwear.ai/operations/external_edit_generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generation_result_id` | body | `number` | no | Generation result ID to edit. |
| `image_url` | body | `string` | no | Direct image URL to edit. |
| `prompt` | body | `string` | yes | Edit prompt. |
