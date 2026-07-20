# Create Dialogue with ElevenLabs

Creates dialogue audio from text in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/text-to-dialogue`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Create Dialogue](https://elevenlabs.io/docs/api-reference/text-to-dialogue/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | Dialogue turns in order. |
| `inputs[].text` | body | `string` | yes | — |
| `inputs[].voice_id` | body | `string` | yes | — |
| `model_id` | body | `string` | yes | — |
| `language_code` | body | `string` | no | — |
| `seed` | body | `number` | no | — |
| `settings` | body | `object` | no | — |
| `settings.speed` | body | `number` | no | — |
| `output_format` | query | `string` | no | — |
| `apply_text_normalization` | query | `string` | no | Use auto, on, or off. |
| `pronunciation_dictionary_locators[]` | body | `array<object>` | no | Pronunciation dictionaries to apply. |
| `pronunciation_dictionary_locators[].id` | body | `string` | no | — |
| `pronunciation_dictionary_locators[].version_id` | body | `string` | no | — |
