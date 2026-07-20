# Speech to Text with Fish Audio

Transcribes audio to text with Fish Audio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/asr`
- **Base URL:** `https://api.fish.audio`
- **Official documentation:** [Speech to Text](https://docs.fish.audio/api-reference/endpoint/openapi-v1/speech-to-text)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio` | body | `file` | yes | Audio file to transcribe. |
| `language` | body | `string` | no | Optional language hint. |
| `ignore_timestamps` | body | `boolean` | no | When true, Fish Audio skips detailed timestamp output. |
