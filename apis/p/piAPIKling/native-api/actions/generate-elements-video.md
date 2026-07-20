# Generate Elements Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Elements Video](https://piapi.ai/docs/kling-api/kling-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Describe the desired elements-based video output. |
| `input.negative_prompt` | body | `string` | no | Describe what Kling should avoid in the elements video. |
| `input.duration` | body | `number` | yes | Elements video length in seconds, typically 5 or 10. |
| `input.aspect_ratio` | body | `string` | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.mode` | body | `string` | no | Elements generation mode, such as std. |
| `input.elements[]` | body | `array<object>` | yes | Array of 1-4 element objects, each with an image_url field. |
