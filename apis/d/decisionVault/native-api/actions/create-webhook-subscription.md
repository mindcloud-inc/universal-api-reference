# Create Webhook Subscription with DecisionVault

Creates a webhook subscription in DecisionVault for an event type.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://api.decisionvault.com/v1`
- **Official documentation:** [Create Webhook Subscription](https://docs.decisionvault.com/create-webhook-subscription-21684970e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | body | `string` | yes | The DecisionVault event type to subscribe to. |
| `headers[]` | body | `array<object>` | no | Optional array of header key-value objects sent with the webhook request. |
| `url` | body | `string` | yes | The webhook endpoint URL to subscribe. |
