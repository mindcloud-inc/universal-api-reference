# Generate Sound Effects with Runway

Creates a sound effect generation task in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sound_effect`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Generate Sound Effects](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1sound_effect/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `number` | no | Optional sound duration in seconds, between 0.5 and 30. |
| `loop` | body | `boolean` | no | Whether the generated sound should loop seamlessly. |
| `model` | body | `string` | yes | Runway currently requires eleven_text_to_sound_v2. |
| `promptText` | body | `string` | yes | Description of the sound effect to generate. |
