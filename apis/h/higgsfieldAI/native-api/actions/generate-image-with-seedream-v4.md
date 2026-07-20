# Generate Image with Seedream v4 with Higgsfield AI

## Endpoint

- **Method:** `POST`
- **Path:** `/bytedance/seedream/v4/text-to-image`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Generate Image with Seedream v4](https://docs.higgsfield.ai/how-to/sdk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the image to generate. |
| `resolution` | body | `string` | no | Generation resolution, for example 2K. |
| `aspect_ratio` | body | `string` | no | Generation aspect ratio, for example 16:9. |
| `camera_fixed` | body | `boolean` | no | Whether the camera should remain fixed. |
| `hf_webhook` | query | `string` | no | Optional public webhook URL for final generation status notifications. |
