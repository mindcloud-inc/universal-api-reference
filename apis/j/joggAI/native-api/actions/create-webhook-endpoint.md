# Create Webhook Endpoint with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/endpoint`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Webhook Endpoint](https://docs.jogg.ai/api-reference/v2/Webhook/AddWebhookEndpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Webhook event types to subscribe to. |
| `status` | body | `string` | yes | Initial webhook status: enabled or disabled. |
| `url` | body | `string` | yes | HTTPS endpoint that should receive webhook events. |
