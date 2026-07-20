# Get TTS Voice with xAI

Retrieves a text-to-speech voice from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/tts/voices/:voice_id`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Get TTS Voice](https://docs.x.ai/developers/rest-api-reference/inference/voice#get-tts-voice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | path | `string` | no | Voice identifier, such as eve or ara. |
