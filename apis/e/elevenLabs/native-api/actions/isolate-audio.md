# Isolate Audio with ElevenLabs

Removes background noise from audio in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/audio-isolation`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Isolate Audio](https://elevenlabs.io/docs/api-reference/audio-isolation/convert)

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
| `preview_b64` | body | `string` | no | — |
