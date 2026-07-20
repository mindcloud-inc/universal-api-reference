# Generate Video from Image with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Video from Image](https://piapi.ai/docs/kling-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image_url` | body | `string` | yes | Source image URL for image-to-video generation. |
| `input.prompt` | body | `string` | yes | Describe the motion or scene you want Kling to generate from the image. |
| `input.negative_prompt` | body | `string` | no | Describe what Kling should avoid in the output. |
| `input.image_tail_url` | body | `string` | no | Optional ending frame image URL when supported by the selected Kling version. |
| `input.duration` | body | `number` | no | Video length in seconds when supported by the selected Kling version and mode. |
| `input.aspect_ratio` | body | `string` | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.mode` | body | `string` | no | Kling generation mode, such as std or pro. |
| `input.version` | body | `string` | no | Kling version, such as 1.6, 2.5, or 2.6. |
