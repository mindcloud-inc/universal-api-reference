# Create Image to Video (Replace) Task with PiAPI/Hunyuan

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Image to Video (Replace) Task](https://piapi.ai/docs/hunyuan-video/txt2video-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.image` | body | `string` | yes |
| `input.prompt` | body | `string` | yes |
| `input.aspect_ratio` | body | `string` | no |
