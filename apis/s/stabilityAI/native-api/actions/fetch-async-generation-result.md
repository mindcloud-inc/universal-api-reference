# Fetch Async Generation Result with Stability AI

Retrieves an asynchronous generation result from Stability AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2beta/results/[:id]`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Fetch Async Generation Result](https://platform.stability.ai/docs/api-reference#tag/Results/paths/~1v2beta~1results~1{id}/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The async generation result id returned by Stability AI. |
