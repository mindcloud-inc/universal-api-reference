# Create Talking Avatar Task with DomoAI

Creates a new talking avatar task in DomoAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/video/talking-avatar`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Create Talking Avatar Task](https://docs.domoai.app/api-reference/ai-video/talking-avatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio.domoai_uri` | body | `string` | yes | A domoai_uri for the driving audio file. |
| `audio.bytes_base64_encoded` | body | `string` | no | Base64-encoded audio bytes. |
| `image.domoai_uri` | body | `string` | no | Optional domoai_uri for the avatar source image. |
| `image.bytes_base64_encoded` | body | `string` | no | Optional base64-encoded avatar source image bytes. |
| `video.domoai_uri` | body | `string` | no | Optional domoai_uri for the avatar source video. |
| `video.bytes_base64_encoded` | body | `string` | no | Optional base64-encoded avatar source video bytes. |
| `seconds` | body | `number` | yes | Output video duration in seconds. |
| `prompt` | body | `string` | no | Optional prompt for generation guidance. |
| `model` | body | `list` | no | The DomoAI talking-avatar model version. Accepted values: `talking-avatar-v1`. |
| `aspect_ratio` | body | `list` | no | Output video aspect ratio. Accepted values: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |
| `callback_url` | body | `string` | no | Optional URL that DomoAI should notify when task status changes. |
