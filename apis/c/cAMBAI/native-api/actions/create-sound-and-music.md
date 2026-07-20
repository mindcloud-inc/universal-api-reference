# Create Sound and Music with CAMB.AI

Creates a new sound or music task in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/text-to-sound`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Sound and Music](https://docs.camb.ai/api-reference/endpoint/create-text-to-sound)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the desired sound or music. |
| `audio_type` | body | `string` | no | Choose whether to generate non-musical sound effects or music. |
| `duration` | body | `number` | no | Desired audio duration in seconds for sound generation. |
