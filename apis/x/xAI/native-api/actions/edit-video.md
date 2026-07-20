# Edit Video with xAI

Edits a video in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/edits`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Edit Video](https://docs.x.ai/developers/rest-api-reference/inference/videos#edit-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Prompt for video editing. |
| `video` | body | `object` | no | Video object with a public MP4 URL. |
