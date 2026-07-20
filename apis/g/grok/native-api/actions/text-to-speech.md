# Text to Speech with Grok

Creates speech audio from text in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tts`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Text to Speech](https://docs.x.ai/developers/rest-api-reference/inference/voice#text-to-speech)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to synthesize. |
| `voice_id` | body | `string` | yes | Voice identifier. |
