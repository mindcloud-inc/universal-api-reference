# Create Text-to-Speech with CAMB.AI

Creates a new text-to-speech task in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/tts`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Text-to-Speech](https://docs.camb.ai/api-reference/endpoint/create-tts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to convert into speech. |
| `voice_id` | body | `number` | yes | Voice identifier from List Voices. |
| `language` | body | `number` | yes | Source language identifier for the speech. |
