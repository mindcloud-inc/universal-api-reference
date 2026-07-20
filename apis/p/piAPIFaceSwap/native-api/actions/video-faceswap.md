# Video Faceswap with PiAPI/FaceSwap

Creates a video faceswap task in PiAPI/FaceSwap.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Video Faceswap](https://piapi.ai/docs/faceswap-api/video-faceswap)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.swap_image` | body | `string` | yes | URL or base64 image containing the replacement face or faces. |
| `input.target_video` | body | `string` | yes | MP4 video URL to process. |
| `input.swap_faces_index` | body | `string` | no | Optional source face indexes for multi-face video swaps. |
| `input.target_faces_index` | body | `string` | no | Optional target face indexes for multi-face video swaps. |
| `config.webhook_config.endpoint` | body | `string` | no | Optional webhook URL for task status notifications. |
| `config.webhook_config.secret` | body | `string` | no | Optional webhook secret returned as x-webhook-secret. |
