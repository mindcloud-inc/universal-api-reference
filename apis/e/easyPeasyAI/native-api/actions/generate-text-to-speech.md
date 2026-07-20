# Generate Text-to-Speech with Easy-Peasy.AI

Generates speech audio in Easy-Peasy.AI from text.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-text-to-speech`
- **Base URL:** `https://easy-peasy.ai`
- **API:** rest
- **Official documentation:** [Generate Text-to-Speech](https://docs.easy-peasy.ai/api-reference/endpoint/generate-tts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to synthesize into speech. |
| `voiceID` | body | `string` | yes | The voice identifier returned by the TTS voice endpoints. |
