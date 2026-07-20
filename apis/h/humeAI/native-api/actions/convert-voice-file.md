# Convert Voice File with Hume AI

Converts uploaded audio in Hume AI and returns a streamed audio file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts/voice_conversion/file`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Convert Voice File](https://dev.hume.ai/reference/text-to-speech-tts/convert-voice-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `audio` | body | `file` | yes |
