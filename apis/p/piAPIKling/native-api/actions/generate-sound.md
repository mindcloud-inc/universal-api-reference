# Generate Sound with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Sound](https://piapi.ai/docs/kling-api/kling-sound-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Describe the sound or soundtrack you want Kling to generate. |
| `input.duration` | body | `number` | no | Requested audio duration in seconds. |
