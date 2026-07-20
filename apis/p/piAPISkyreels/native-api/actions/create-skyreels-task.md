# Create Skyreels Task with PiAPI/Skyreels

Creates a new Skyreels task in PiAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Skyreels Task](https://piapi.ai/docs/skyreels-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Prompt describing the motion or video to generate. |
| `input.image` | body | `string` | yes | Source image URL for the Skyreels img2video task. |
| `input.negative_prompt` | body | `string` | no | Optional prompt describing what to avoid. |
| `input.aspect_ratio` | body | `list` | no | Optional output aspect ratio. Accepted values: `0`, `1`, `2`. |
| `input.guidance_scale` | body | `number` | no | Optional guidance scale value. |
