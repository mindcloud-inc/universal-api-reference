# Create Sora2 Pro Text to Video Task with PiAPI/Sora

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Sora2 Pro Text to Video Task](https://piapi.ai/docs/sora2-pro-api/text-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Text prompt for the Sora2 Pro video. |
| `input.aspect_ratio` | body | `string` | no | Aspect ratio sent to PiAPI. |
| `input.resolution` | body | `list` | no | Sora2 Pro output resolution. Accepted values: `1080p`, `720p`. |
| `input.duration` | body | `number` | no | Video duration in seconds. |
