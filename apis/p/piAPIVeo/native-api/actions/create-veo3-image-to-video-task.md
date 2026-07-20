# Create Veo3 Image to Video Task with PiAPI/Veo

Creates a Veo 3 image-to-video task in PiAPI/Veo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Veo3 Image to Video Task](https://piapi.ai/docs/veo3-api/image-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image_url` | body | `string` | yes | — |
| `input.prompt` | body | `string` | yes | — |
| `task_type` | body | `string` | yes | Use veo3-video or veo3-video-fast. |
| `input.aspect_ratio` | body | `string` | no | — |
| `input.duration` | body | `string` | no | — |
| `input.resolution` | body | `string` | no | — |
| `input.generate_audio` | body | `boolean` | no | — |
