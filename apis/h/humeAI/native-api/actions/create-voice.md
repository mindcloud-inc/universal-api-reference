# Create Voice with Hume AI

Creates a custom voice in Hume AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts/voices`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create Voice](https://dev.hume.ai/reference/voices/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generation_id` | body | `string` | yes | TTS generation ID to save as a reusable voice. |
| `name` | body | `string` | yes | Name of the voice to create. |
