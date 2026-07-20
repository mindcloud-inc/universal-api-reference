# Text To Speech with Runway

Creates a text-to-speech generation task in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text_to_speech`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Text To Speech](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1text_to_speech/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Runway currently requires eleven_multilingual_v2. |
| `promptText` | body | `string` | yes | Detailed prompt text to synthesize into speech. |
| `voice` | body | `object` | yes | Voice object with type runway-preset and presetId. |
