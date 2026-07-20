# Create Transcription with Gladia

Creates a transcription job in Gladia.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/transcription`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Create Transcription](https://docs.gladia.io/api-reference/v2/transcription/init)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Gladia file URL or external audio URL for the transcription job. |
