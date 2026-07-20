# Get Legacy Upscale Result with Dreamstudio

Retrieves a legacy upscale result from Dreamstudio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2alpha/generation/stable-image/upscale/result/:id`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Get Legacy Upscale Result](https://platform.stability.ai/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Async upscale job identifier. |
