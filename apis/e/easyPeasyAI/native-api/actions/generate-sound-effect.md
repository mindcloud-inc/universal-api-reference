# Generate Sound Effect with Easy-Peasy.AI

Generates a sound effect in Easy-Peasy.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-sound`
- **Base URL:** `https://easy-peasy.ai`
- **API:** rest
- **Official documentation:** [Generate Sound Effect](https://docs.easy-peasy.ai/api-reference/endpoint/generate-sound)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | The text prompt describing the sound effect to generate. |
| `duration` | body | `number` | no | Optional target duration for the sound effect. |
| `prompt_influence` | body | `number` | no | Optional prompt adherence level from 0.0 to 1.0. |
