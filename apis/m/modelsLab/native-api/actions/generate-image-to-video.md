# Generate Image To Video with ModelsLab

Creates a video from an image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/video/img2video`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Image To Video](https://docs.modelslab.com/video-api/img-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Source image URL for video generation. |
| `prompt` | body | `string` | no | Motion prompt for image-to-video generation. |
