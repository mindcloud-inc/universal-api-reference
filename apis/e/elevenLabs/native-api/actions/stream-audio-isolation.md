# Stream Audio Isolation with ElevenLabs

Streams audio with background noise removed from ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/audio-isolation/stream`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Stream Audio Isolation](https://elevenlabs.io/docs/api-reference/audio-isolation/stream)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio` | body | `file` | yes | Audio file to isolate. |
| `file_format` | body | `string` | no | — |
