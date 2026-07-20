# Generate Text To Video with ModelsLab

Creates a video from text in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/video/text2video`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Text To Video](https://docs.modelslab.com/video-api/text-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | body | `string` | no | Video model ID, for example wan2.2. |
| `prompt` | body | `string` | no | Text prompt describing the generated video. |
