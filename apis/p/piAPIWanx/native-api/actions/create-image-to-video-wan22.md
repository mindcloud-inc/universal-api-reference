# Create Image to Video (Wan 2.2) with PiAPI/Wanx

Creates an image-to-video task in PiAPI/Wanx.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Image to Video (Wan 2.2)](https://piapi.ai/docs/wanx-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | no | Describe the Wan 2.2 image-to-video motion you want to generate. |
| `input.negative_prompt` | body | `string` | no | Describe elements you want Wan 2.2 to avoid. |
| `input.image` | body | `string` | yes | Image URL or base64 image data for Wan 2.2 image-to-video generation. |
