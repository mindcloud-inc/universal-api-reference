# Generate Text to Speech File Data with Hamsa

Generates text-to-speech file data with Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/realtime/tts`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Generate Text to Speech File Data](https://docs.tryhamsa.com/api-reference/endpoint/generate-text-to-speech-file-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dialect` | body | `string` | no |
| `mulaw` | body | `boolean` | no |
| `speaker` | body | `string` | yes |
| `text` | body | `string` | yes |
