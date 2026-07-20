# Create Webhook Subscription with DataForB2B

Creates a webhook subscription in DataForB2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Create Webhook Subscription](https://docs.dataforb2b.ai/api-reference/webhooks-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | HTTPS endpoint that should receive webhook deliveries. |
| `event_types` | body | `object<string>` | yes | List of event types to subscribe to. |
