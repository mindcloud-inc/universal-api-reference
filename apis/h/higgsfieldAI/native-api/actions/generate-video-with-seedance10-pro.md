# Generate Video with Seedance 1.0 Pro with Higgsfield AI

Creates a video with Seedance 1.0 Pro in Higgsfield AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/bytedance/seedance/v1/pro/image-to-video`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Generate Video with Seedance 1.0 Pro](https://docs.higgsfield.ai/guides/video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL to animate into a video. |
| `prompt` | body | `string` | yes | Motion prompt describing the video animation. |
| `hf_webhook` | query | `string` | no | Optional public webhook URL for final generation status notifications. |
