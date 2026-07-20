# Get Async Upscale Result with Stable Diffusion

Retrieves an asynchronous upscale result from Stable Diffusion.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2alpha/generation/stable-image/upscale/result/{id}`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Get Async Upscale Result](https://platform.stability.ai/docs/api-reference#tag/v2alpha%2Fgeneration/paths/~1v2alpha~1generation~1stable-image~1upscale~1result~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Upscale generation identifier. |
