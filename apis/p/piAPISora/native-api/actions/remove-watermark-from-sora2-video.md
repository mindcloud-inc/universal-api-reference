# Remove Watermark from Sora2 Video with PiAPI/Sora

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Remove Watermark from Sora2 Video](https://piapi.ai/docs/sora2-api/remove-watermark)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.video_url` | body | `string` | yes | URL of the Sora video that still has a watermark. |
