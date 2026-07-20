# Generate Speech to Text Transcription with Hamsa

Generates a speech-to-text transcription with Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/realtime/stt`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Generate Speech to Text Transcription](https://docs.tryhamsa.com/api-reference/endpoint/generate-speech-to-text-transcription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audioBase64` | body | `string` | no | — |
| `audioList[]` | body | `array<number>` | no | Send multiple values as a array. |
| `eosThreshold` | body | `number` | no | — |
| `isEosEnabled` | body | `boolean` | no | — |
| `language` | body | `string` | no | — |
