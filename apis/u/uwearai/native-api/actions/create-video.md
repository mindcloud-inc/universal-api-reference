# Create Video with Uwear.ai

Creates a video generation in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/generation-video`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Create Video](https://docs.dev.uwear.ai/operations/external_video_generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `number` | no | Optional video duration in seconds. |
| `generation_result_id` | body | `number` | no | Generation result ID to animate. |
| `image_url` | body | `string` | no | Direct image URL to animate. |
| `model_name` | body | `string` | no | Optional Uwear video model name. |
| `prompt` | body | `string` | no | Optional motion prompt for the video. |
| `resolution` | body | `string` | no | Optional output resolution. |
