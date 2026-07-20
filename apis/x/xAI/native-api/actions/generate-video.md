# Generate Video with xAI

Creates a video in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/generations`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Generate Video](https://docs.x.ai/developers/rest-api-reference/inference/videos#generate-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Video generation model name. |
| `prompt` | body | `string` | no | Prompt for video generation. |
| `duration` | body | `number` | no | Video duration in seconds. |
