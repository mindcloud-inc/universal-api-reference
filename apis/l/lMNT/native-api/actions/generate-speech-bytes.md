# Generate Speech (Bytes) with LMNT

Creates streaming speech audio from text in LMNT.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/speech/bytes`
- **Base URL:** `https://api.lmnt.com`
- **Official documentation:** [Generate Speech (Bytes)](https://docs.lmnt.com/api-reference/speech/synthesize-speech-bytes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | no | Optional output audio format such as mp3, wav, webm, ulaw, pcm_s16le, pcm_f32le, or aac. |
| `language` | body | `string` | no | Optional ISO 639-1 language code. Defaults to auto-detection. |
| `sample_rate` | body | `number` | no | Optional output sample rate in Hz. |
| `seed` | body | `number` | no | Optional seed to reproduce a take. |
| `text` | body | `string` | yes | The text to synthesize. LMNT documents a maximum of 5000 characters per request. |
| `voice` | body | `string` | yes | The voice id to use for synthesis. |
