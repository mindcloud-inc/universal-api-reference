# Generate Streamed Text to Speech File Data with Hamsa

Generates streamed text-to-speech audio data with Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/realtime/tts-stream`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Generate Streamed Text to Speech File Data](https://docs.tryhamsa.com/api-reference/endpoint/generate-streamed-text-to-speech-file-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dialect` | body | `string` | no |
| `mulaw` | body | `boolean` | no |
| `speaker` | body | `string` | yes |
| `text` | body | `string` | yes |
