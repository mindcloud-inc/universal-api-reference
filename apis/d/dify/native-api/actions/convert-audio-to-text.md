# Convert Audio to Text with Dify

Creates a text transcription from audio in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/audio-to-text`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Convert Audio to Text](https://docs.dify.ai/api-reference/tts/convert-audio-to-text)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Audio file to transcribe. |
| `user` | body | `string` | no | User identifier. |
