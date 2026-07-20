# Get Generation Result with Stable Diffusion

Retrieves a generation result from Stable Diffusion.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2beta/results/{id}`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Get Generation Result](https://platform.stability.ai/docs/api-reference#tag/Results/paths/~1v2beta~1results~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Generation identifier returned by an asynchronous Stability endpoint. |
