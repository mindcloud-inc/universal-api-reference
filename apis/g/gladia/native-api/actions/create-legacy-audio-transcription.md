# Create Legacy Audio Transcription with Gladia

Creates a legacy audio transcription job in Gladia.

## Endpoint

- **Method:** `POST`
- **Path:** `/audio/text/audio-transcription`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Create Legacy Audio Transcription](https://docs.gladia.io/chapters/pre-recorded-stt/migration-from-v1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Legacy V1 audio URL input. |
