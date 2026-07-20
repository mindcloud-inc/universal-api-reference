# Create Text-to-Speech Job with deAPI

Creates a text-to-speech job in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2audio`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | no | Audio output format such as mp3 or flac. |
| `lang` | body | `string` | no | Language code such as en-us. |
| `mode` | body | `string` | no | TTS mode. Use custom_voice for preset voices. |
| `model` | body | `string` | no | Speech model slug from List Models. |
| `sample_rate` | body | `string` | no | Sample rate for generated audio. |
| `speed` | body | `string` | no | Speech speed multiplier. |
| `text` | body | `string` | no | Text to convert to speech. |
| `voice` | body | `string` | no | Voice slug for custom_voice mode. |
