# Image Faceswap with PiAPI/FaceSwap

Creates an image faceswap task in PiAPI/FaceSwap.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Image Faceswap](https://piapi.ai/docs/api-10275990)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.target_image` | body | `string` | yes | URL or base64 image that will receive the swapped face. |
| `input.swap_image` | body | `string` | yes | URL or base64 image that provides the face to swap in. |
| `config.webhook_config.endpoint` | body | `string` | no | Optional webhook URL for task status notifications. |
| `config.webhook_config.secret` | body | `string` | no | Optional webhook secret returned as x-webhook-secret. |
