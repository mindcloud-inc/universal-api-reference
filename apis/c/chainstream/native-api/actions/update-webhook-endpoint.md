# Update Webhook Endpoint with Chainstream

Updates a webhook endpoint in Chainstream.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/webhook/endpoint`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Update Webhook Endpoint](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointId` | body | `string` | yes | Endpoint ID |
| `url` | body | `string` | no | Webhook destination URL |
| `channels[]` | body | `array<string>` | no | Webhook event channels to subscribe to |
| `description` | body | `string` | no | Endpoint description |
| `disabled` | body | `boolean` | no | Whether the endpoint is disabled |
| `filter` | body | `string` | no | Event filter configuration |
| `filterTypes[]` | body | `array<string>` | no | Event type filters |
| `metadata` | body | `object` | no | Endpoint metadata |
| `rateLimit` | body | `number` | no | Rate limit for the endpoint |
