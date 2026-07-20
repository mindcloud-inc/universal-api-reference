# Generate Video with Kling 2.1 Pro with Higgsfield AI

Creates a video with Kling 2.1 Pro in Higgsfield AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling-video/v2.1/pro/image-to-video`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Generate Video with Kling 2.1 Pro](https://docs.higgsfield.ai/guides/video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL to animate into a video. |
| `prompt` | body | `string` | yes | Motion prompt describing the video animation. |
| `hf_webhook` | query | `string` | no | Optional public webhook URL for final generation status notifications. |
