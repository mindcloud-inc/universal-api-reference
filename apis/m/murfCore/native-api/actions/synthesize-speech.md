# Synthesize Speech with Murf Core

Synthesizes speech from text in Murf Core.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/speech/generate`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Synthesize Speech](https://murf.ai/api/docs/api-reference/text-to-speech/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to synthesize into speech. |
| `voiceId` | body | `string` | yes | Voice identifier from the List Voices action. |
| `locale` | body | `string` | no | Optional target locale for multi-native generation. |
| `format` | body | `string` | no | Optional output format such as WAV, MP3, or FLAC. |
| `encodeAsBase64` | body | `boolean` | no | Return audio inline as base64 instead of a hosted URL. |
