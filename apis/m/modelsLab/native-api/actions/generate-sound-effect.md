# Generate Sound Effect with ModelsLab

Creates a sound effect in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/voice/sfx`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Sound Effect](https://docs.modelslab.com/voice-cloning/sfx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `string` | no | Sound effect duration in seconds. |
| `prompt` | body | `string` | no | Description of the sound effect to generate. |
