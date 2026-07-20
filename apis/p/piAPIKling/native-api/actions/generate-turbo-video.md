# Generate Turbo Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Turbo Video](https://piapi.ai/docs/kling-api/kling-turbo-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Describe the turbo video you want Kling to generate. |
| `input.negative_prompt` | body | `string` | no | Describe what Kling Turbo should avoid in the output. |
| `input.start_image_url` | body | `string` | no | Optional starting frame image URL. |
| `input.end_image_url` | body | `string` | no | Optional ending frame image URL. |
| `input.duration` | body | `number` | no | Turbo video length in seconds. |
| `input.aspect_ratio` | body | `string` | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.mode` | body | `string` | no | Turbo generation mode, such as pro. |
| `input.version` | body | `string` | no | Turbo version, such as 2.5-turbo. |
