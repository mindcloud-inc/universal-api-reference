# Generate Omni Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Omni Video](https://piapi.ai/docs/kling-api/kling-3-omni-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Describe the omni video you want Kling to generate. |
| `input.resolution` | body | `string` | yes | Omni output resolution, such as 720p or 1080p. |
| `input.duration` | body | `number` | yes | Omni video length in seconds. |
| `input.aspect_ratio` | body | `string` | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.enable_audio` | body | `boolean` | no | Enable native audio generation in the omni output. |
