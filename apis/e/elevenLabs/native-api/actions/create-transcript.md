# Create Transcript with ElevenLabs

Creates a transcript from audio or video in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/speech-to-text`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Create Transcript](https://elevenlabs.io/docs/api-reference/speech-to-text/convert)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloud_storage_url` | body | `string` | yes | A public audio file URL for transcription. |
| `model_id` | body | `string` | yes | The speech-to-text model identifier. |
| `language_code` | body | `string` | no | — |
| `tag_audio_events` | body | `boolean` | no | — |
