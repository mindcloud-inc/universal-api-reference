# Get Analytics with fal.ai

Retrieves model endpoint analytics from fal.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/analytics`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Get Analytics](https://fal.ai/docs/platform-apis/v1/models/analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_id` | query | `string` | yes | Exact fal.ai endpoint ID to analyze. |
