# Fetch Creative Upscale Result with Stability AI

Retrieves a creative upscale result from Stability AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2beta/stable-image/upscale/creative/result/[:id]`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Fetch Creative Upscale Result](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1creative~1result~1{id}/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Creative Upscale result id returned by Stability AI. |
