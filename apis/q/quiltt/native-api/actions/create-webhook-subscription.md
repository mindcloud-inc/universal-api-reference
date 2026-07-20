# Create Webhook Subscription with Quiltt

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks/subscriptions`
- **Base URL:** `https://api.quiltt.io`
- **Official documentation:** [Create Webhook Subscription](https://www.quiltt.dev/webhooks/setup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventTypes` | body | `list<string>` | yes | List of webhook event types to subscribe to. Send multiple values as a array. |
| `name` | body | `string` | yes | Webhook subscription name. |
| `targetUrl` | body | `string` | yes | URL that receives webhook deliveries. |
