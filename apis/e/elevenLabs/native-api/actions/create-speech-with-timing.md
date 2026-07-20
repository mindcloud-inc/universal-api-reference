# Create Speech with Timing with ElevenLabs

Creates speech audio with timestamps in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/text-to-speech/:voice_id/with-timestamps`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Create Speech with Timing](https://elevenlabs.io/docs/api-reference/text-to-speech/convert-with-timestamps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | path | `string` | yes | The voice identifier. |
| `text` | body | `string` | yes | The text to synthesize. |
| `model_id` | body | `string` | no | — |
| `language_code` | body | `string` | no | — |
| `seed` | body | `number` | no | — |
| `output_format` | query | `string` | no | — |
| `enable_logging` | query | `boolean` | no | — |
