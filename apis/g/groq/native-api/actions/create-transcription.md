# Create Transcription with Groq

Creates a transcription from audio in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/audio/transcriptions`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Transcription](https://console.groq.com/docs/api-reference#audio-transcription)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | no |
| `url` | body | `string` | no |
| `model` | body | `string` | yes |
| `prompt` | body | `string` | no |
| `response_format` | body | `list` | no |
| `language` | body | `string` | no |
| `temperature` | body | `number` | no |
| `timestamp_granularities[]` | body | `array<string>` | no |
