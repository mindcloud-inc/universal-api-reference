# Video Upscale with PiAPI/Toolkit

Creates a video-upscale task in PiAPI/Toolkit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Video Upscale](https://piapi.ai/docs/tools/video-upscale-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.video` | body | `string` | yes | Doc-backed PiAPI field for Video Upscale. |
