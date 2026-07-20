# Create Text To Speech with xAI

Creates text-to-speech audio in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/tts`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Create Text To Speech](https://docs.x.ai/developers/rest-api-reference/inference/voice#text-to-speech)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | Text to convert to speech. |
| `voice_id` | body | `string` | no | Voice identifier, such as eve or ara. |
| `language` | body | `string` | no | BCP-47 language code or auto. |
