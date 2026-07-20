# Generate Text To Speech with ModelsLab

Creates speech audio from text in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/voice/text_to_speech`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Text To Speech](https://docs.modelslab.com/voice-cloning/text-to-speech)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Text to convert to speech. |
| `voice_id` | body | `string` | no | Voice ID to use for speech generation. |
