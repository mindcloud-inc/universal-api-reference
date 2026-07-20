# Create Sora2 Text to Video Task with PiAPI/Sora

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Sora2 Text to Video Task](https://piapi.ai/docs/sora2-api/text-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Text prompt for the Sora2 video. |
| `input.aspect_ratio` | body | `string` | no | Aspect ratio sent to PiAPI. |
| `input.duration` | body | `number` | no | Video duration in seconds. |
