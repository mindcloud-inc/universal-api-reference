# Image Upscale (Super Resolution) API with PiAPI/Toolkit

Creates an image-upscale task in PiAPI/Toolkit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Image Upscale (Super Resolution) API](https://piapi.ai/docs/image-editing-api/super-resolution-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image` | body | `string` | yes | Doc-backed PiAPI field for Image Upscale (Super Resolution) API. |
| `input.scale` | body | `number` | yes | Doc-backed PiAPI field for Image Upscale (Super Resolution) API. |
| `input.face_enhance` | body | `boolean` | no | Doc-backed PiAPI field for Image Upscale (Super Resolution) API. |
