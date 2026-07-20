# Kling TTS with CometAPI

Creates speech audio with Kling in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/audio/tts`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling TTS](https://apidoc.cometapi.com/api/video/kling/tts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to synthesize. |
| `voice_id` | body | `string` | yes | Voice identifier. |
| `voice_language` | body | `string` | yes | Voice language code. |
