# Text To Speech with Uberduck

Creates speech audio in Uberduck from input text.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text-to-speech`
- **Base URL:** `https://api.uberduck.ai`
- **Official documentation:** [Text To Speech](https://docs.uberduck.ai/api-reference/text-to-speech-v-1-text-to-speech-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to convert to speech. |
| `voice` | body | `string` | yes | The voice ID to use for speech generation. |
| `model` | body | `string` | no | Optional model ID. If omitted, Uberduck selects a compatible default model. |
| `output_format` | body | `string` | no | Optional output format such as mp3. |
| `extended` | body | `string` | no | Optional JSON object for shared advanced controls such as speed, pitch, or emotion. |
| `model_specific` | body | `string` | no | Optional JSON object for model-specific controls such as Polly engine or Google speaking rate. |
