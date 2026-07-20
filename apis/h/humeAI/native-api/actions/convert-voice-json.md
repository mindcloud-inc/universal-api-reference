# Convert Voice JSON with Hume AI

Converts uploaded audio in Hume AI and returns streamed JSON.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts/voice_conversion/json`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Convert Voice JSON](https://dev.hume.ai/reference/text-to-speech-tts/convert-voice-json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `audio` | body | `file` | yes |
