# Create Webhook Endpoint with Chainstream

Creates a webhook endpoint in Chainstream.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/webhook/endpoint`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Create Webhook Endpoint](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL |
| `channels[]` | body | `array<string>` | no | Webhook event channels to subscribe to |
| `description` | body | `string` | no | Endpoint description |
| `disabled` | body | `boolean` | no | Whether the endpoint is disabled |
| `filter` | body | `string` | no | Event filter configuration |
| `filterTypes[]` | body | `array<string>` | no | Event type filters |
| `metadata` | body | `object` | no | Endpoint metadata |
| `rateLimit` | body | `number` | no | Rate limit for the endpoint |
| `secret` | body | `string` | no | Endpoint signing secret |
