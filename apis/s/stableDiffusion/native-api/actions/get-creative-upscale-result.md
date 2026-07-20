# Get Creative Upscale Result with Stable Diffusion

Retrieves a creative upscale result from Stable Diffusion.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2beta/stable-image/upscale/creative/result/{id}`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Get Creative Upscale Result](https://platform.stability.ai/docs/api-reference#tag/Results/paths/~1v2beta~1stable-image~1upscale~1creative~1result~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Generation identifier returned by creative upscale. |
