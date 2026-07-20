# Create Transcription with Orq.ai

Creates an audio transcription in Orq.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/router/audio/transcriptions`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Create Transcription](https://docs.orq.ai/reference/audio/create-transcription)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `model` | body | `string` | yes |
