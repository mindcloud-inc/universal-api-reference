# List Serverless Requests By Endpoint with fal.ai

Retrieves requests for fal.ai serverless endpoints.

## Endpoint

- **Method:** `GET`
- **Path:** `/serverless/requests/by-endpoint`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [List Serverless Requests By Endpoint](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_id` | query | `string` | yes | Exact fal.ai endpoint ID to inspect requests for. |
