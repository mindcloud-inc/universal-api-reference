# Stream Speech JSON with Hume AI

Streams synthesized speech from Hume AI as JSON.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts/stream/json`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Stream Speech JSON](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-json-streaming)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `utterances[0].text` | body | `string` | yes |
| `utterances[0].voice.name` | body | `string` | no |
| `utterances[0].voice.provider` | body | `string` | no |
| `utterances[0].description` | body | `string` | no |
