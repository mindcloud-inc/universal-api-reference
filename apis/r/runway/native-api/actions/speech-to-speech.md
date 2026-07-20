# Speech To Speech with Runway

Creates a speech-to-speech generation task in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/speech_to_speech`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Speech To Speech](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1speech_to_speech/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media` | body | `object` | yes | Audio or video media object with type and uri. |
| `model` | body | `string` | yes | Runway currently requires eleven_multilingual_sts_v2. |
| `voice` | body | `object` | yes | Voice object with type runway-preset and presetId. |
