# List Requests By Endpoint with fal.ai

Retrieves requests for fal.ai model endpoints.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/requests/by-endpoint`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [List Requests By Endpoint](https://fal.ai/docs/platform-apis/v1/models/requests/by-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_id` | query | `string` | yes | Exact fal.ai endpoint ID to inspect requests for. |
