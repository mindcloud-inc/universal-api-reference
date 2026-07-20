# Create Transcription with Mistral AI

Creates an audio transcription in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/audio/transcriptions`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Create Transcription](https://docs.mistral.ai/api/endpoint/audio/transcriptions#operation-audio_api_v1_transcriptions_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | ID of the transcription model to use. |
| `file` | body | `file` | no | Audio file object to transcribe. |
| `file_url` | body | `string` | no | URL of the audio file to transcribe. |
| `file_id` | body | `string` | no | ID of an uploaded file to transcribe. |
| `language` | body | `string` | no | Language hint for the audio. |
| `temperature` | body | `number` | no | Sampling temperature for transcription decoding. |
| `stream` | body | `boolean` | no | Whether to stream partial transcription progress. |
| `diarize` | body | `boolean` | no | Whether to enable speaker diarization. |
| `context_bias[]` | body | `array<string>` | no | Optional context-bias phrases. |
| `timestamp_granularities[]` | body | `array<string>` | no | Timestamp granularities to include in the response. |
