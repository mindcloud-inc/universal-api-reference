# Create Sound Effect with ElevenLabs

Creates sound effect audio from text in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/sound-generation`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Create Sound Effect](https://elevenlabs.io/docs/api-reference/text-to-sound-effects/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text prompt describing the sound effect to generate. |
| `duration_seconds` | body | `number` | no | Approximate desired length of the generated sound effect in seconds. |
| `prompt_influence` | body | `number` | no | How strongly the prompt should influence the output. |
| `loop` | body | `boolean` | no | Whether the generated sound effect should loop seamlessly. |
| `model_id` | body | `string` | no | Optional sound generation model identifier. |
| `output_format` | query | `string` | no | Requested audio output format. |
