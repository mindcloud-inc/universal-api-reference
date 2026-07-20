# Create Image to Video with Camera Control with PiAPI/Wanx

Creates a camera-controlled video task in PiAPI/Wanx.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Image to Video with Camera Control](https://piapi.ai/docs/wanx-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | no | Describe the video you want WanX to generate. |
| `input.negative_prompt` | body | `string` | no | Describe elements you want the model to avoid. |
| `input.image` | body | `string` | yes | Image URL or base64 image data for WanX image-to-video generation. |
| `input.control_camera_settings[]` | body | `array<object>` | yes | Array of camera control objects such as [{"type":"static","config":{"horizontal":0,"vertical":0,"pan":0,"tilt":0,"roll":0,"zoom":0}}]. |
