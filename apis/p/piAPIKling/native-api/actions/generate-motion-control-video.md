# Generate Motion Control Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Motion Control Video](https://piapi.ai/docs/kling-api/kling-motion-control-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image_url` | body | `string` | yes | Source image URL for motion control generation. |
| `input.video_url` | body | `string` | no | Optional motion reference video URL. Use this or Preset Motion. |
| `input.preset_motion` | body | `string` | no | Preset motion reference name. Use this or Video URL. |
| `input.motion_direction` | body | `string` | no | Motion direction mode from the PiAPI motion control contract. |
| `input.keep_original_sound` | body | `boolean` | no | Keep the original sound from the motion reference when supported. |
| `input.mode` | body | `string` | no | Motion control generation mode, such as std or pro. |
| `input.version` | body | `string` | no | Supported motion control version, such as 2.6 or 3.0. |
