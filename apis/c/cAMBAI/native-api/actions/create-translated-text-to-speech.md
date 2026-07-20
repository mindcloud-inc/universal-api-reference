# Create Translated Text-to-Speech with CAMB.AI

Creates a translated text-to-speech task in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/translated-tts`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Translated Text-to-Speech](https://docs.camb.ai/api-reference/endpoint/create-translated-tts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to translate and synthesize. |
| `voice_id` | body | `number` | yes | Voice identifier from List Voices. |
| `source_language` | body | `number` | yes | Source language identifier from Get Source Languages. |
| `target_language` | body | `number` | yes | Target language identifier from Get Target Languages. |
