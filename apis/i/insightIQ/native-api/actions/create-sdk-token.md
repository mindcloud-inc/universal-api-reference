# Create SDK Token with InsightIQ

Creates a new SDK token in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sdk-tokens`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create SDK Token](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products[]` | body | `array<string>` | yes | Products to enable in the SDK token. |
| `user_id` | body | `string` | yes | InsightIQ user identifier used to mint the SDK token. |
