# Create Pre-recorded Transcription with Gladia

Creates a pre-recorded transcription job in Gladia.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/pre-recorded`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Create Pre-recorded Transcription](https://docs.gladia.io/api-reference/v2/pre-recorded/init)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Publicly accessible audio URL for the new pre-recorded transcription job. |
