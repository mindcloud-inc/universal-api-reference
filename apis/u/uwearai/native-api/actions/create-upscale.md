# Create Upscale with Uwear.ai

Creates an upscale generation in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/generation-upscale`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Create Upscale](https://docs.dev.uwear.ai/operations/external_upscale_generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generation_result_id` | body | `number` | no | Generation result ID to upscale. |
| `image_url` | body | `string` | no | Direct image URL to upscale. |
| `model_name` | body | `string` | no | Optional Uwear model name for the upscale request. |
