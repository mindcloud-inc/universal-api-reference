# Submit Generation Request with Higgsfield AI

Submits a generation request to Higgsfield AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/{modelId}`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Submit Generation Request](https://docs.higgsfield.ai/how-to/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | Higgsfield model identifier, for example higgsfield-ai/soul/standard. |
| `prompt` | body | `string` | no | Text prompt or motion prompt sent to the selected model. |
| `aspect_ratio` | body | `string` | no | Generation aspect ratio, for example 16:9. |
| `resolution` | body | `string` | no | Generation resolution, for example 720p or 2K. |
| `image_url` | body | `string` | no | Source image URL for image-to-video or image-editing models. |
| `duration` | body | `number` | no | Requested video duration in seconds when supported by the model. |
| `camera_fixed` | body | `boolean` | no | Whether the camera should remain fixed when supported by the model. |
| `hf_webhook` | query | `string` | no | Optional public webhook URL for final generation status notifications. |
