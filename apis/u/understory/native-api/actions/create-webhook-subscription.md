# Create Webhook Subscription with Understory

Creates a new webhook subscription in Understory.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhook-subscriptions`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Create Webhook Subscription](https://developer.understory.io/apis/webhook/createwebhooksubscription.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to send webhook events to. |
| `event_types[]` | body | `array<string>` | yes | One or more event types to subscribe to. |
| `state` | body | `list` | yes | The state of the subscription. Accepted values: `0`, `1`. |
| `metadata` | body | `object` | no | Optional custom metadata object for the subscription. |
