# Create Transcription with Open AI

Transcribes audio in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/audio/transcriptions`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Transcription](https://developers.openai.com/api/reference/resources/audio/subresources/transcriptions/methods/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Audio file input for transcription. |
| `model` | body | `list` | yes | Transcription model ID. |
