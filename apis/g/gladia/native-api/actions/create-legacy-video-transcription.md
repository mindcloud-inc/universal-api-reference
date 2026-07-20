# Create Legacy Video Transcription with Gladia

Creates a legacy video transcription job in Gladia.

## Endpoint

- **Method:** `POST`
- **Path:** `/video/text/video-transcription`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Create Legacy Video Transcription](https://api.gladia.io/openapi.json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_url` | body | `string` | yes | Legacy V1 video URL input. |
