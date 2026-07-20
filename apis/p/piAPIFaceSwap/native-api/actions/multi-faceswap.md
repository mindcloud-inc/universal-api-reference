# Multi Faceswap with PiAPI/FaceSwap

Creates a multi-face faceswap task in PiAPI/FaceSwap.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Multi Faceswap](https://piapi.ai/docs/multi-face-swap/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.swap_image` | body | `string` | yes | URL or base64 image containing the source faces. |
| `input.target_image` | body | `string` | yes | URL or base64 image containing the faces to replace. |
| `input.swap_faces_index` | body | `string` | no | Comma-separated source face indexes in PiAPI's detected order. |
| `input.target_faces_index` | body | `string` | no | Comma-separated target face indexes in PiAPI's detected order. |
| `config.webhook_config.endpoint` | body | `string` | no | Optional webhook URL for task status notifications. |
| `config.webhook_config.secret` | body | `string` | no | Optional webhook secret returned as x-webhook-secret. |
