# Get Pricing with fal.ai

Retrieves model endpoint pricing from fal.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/pricing`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Get Pricing](https://fal.ai/docs/platform-apis/v1/models/pricing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_id` | query | `string` | yes | Exact fal.ai endpoint ID to price. |
