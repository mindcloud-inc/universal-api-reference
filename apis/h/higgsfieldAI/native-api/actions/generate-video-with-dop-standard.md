# Generate Video with DoP Standard with Higgsfield AI

Creates a video with DoP Standard in Higgsfield AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/higgsfield-ai/dop/standard`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Generate Video with DoP Standard](https://docs.higgsfield.ai/guides/video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL to animate into a video. |
| `prompt` | body | `string` | yes | Motion prompt describing the video animation. |
| `duration` | body | `number` | no | Requested video duration in seconds. |
| `hf_webhook` | query | `string` | no | Optional public webhook URL for final generation status notifications. |
