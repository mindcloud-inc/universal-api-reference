# Generate Video from Text with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Video from Text](https://piapi.ai/docs/kling-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Describe the video you want Kling to generate. |
| `input.negative_prompt` | body | `string` | no | Describe what Kling should avoid in the output. |
| `input.duration` | body | `number` | no | Video length in seconds when supported by the selected Kling version and mode. |
| `input.aspect_ratio` | body | `string` | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.mode` | body | `string` | no | Kling generation mode, such as std or pro. |
| `input.version` | body | `string` | no | Kling version, such as 1.6, 2.5, or 2.6. |
| `input.enable_audio` | body | `boolean` | no | Enable native audio generation when the selected Kling version supports it. |
| `input.cfg_scale` | body | `number` | no | Guidance scale for Kling video generation. |
