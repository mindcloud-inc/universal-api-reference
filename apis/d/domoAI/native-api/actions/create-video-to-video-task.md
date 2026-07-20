# Create Video to Video Task with DomoAI

Creates a new video-to-video task in DomoAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/video/video2video`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Create Video to Video Task](https://docs.domoai.app/api-reference/ai-video/video-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `list` | yes | The DomoAI video-to-video model version. Accepted values: `anime-v1.2`, `anime-v10`, `anime-v5.5`, `anime-v9.1`, `illustration-v19`, `illustration-v20`, `illustration-v8.1`, `illustration-v9.1`. |
| `video.domoai_uri` | body | `string` | yes | A domoai_uri from the Upload File action. |
| `video.bytes_base64_encoded` | body | `string` | no | Base64-encoded video bytes. |
| `seconds` | body | `number` | yes | Output video duration in seconds. |
| `prompt` | body | `string` | no | Optional prompt describing the desired style transformation. |
| `aspect_ratio` | body | `list` | no | Output video aspect ratio. Accepted values: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |
| `callback_url` | body | `string` | no | Optional URL that DomoAI should notify when task status changes. |
