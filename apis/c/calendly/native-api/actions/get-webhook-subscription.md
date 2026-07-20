# Get Webhook Subscription with Calendly

Retrieves a webhook subscription from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook_subscriptions/:webhook_uuid`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Get Webhook Subscription](https://developer.calendly.com/api-docs/4d800dc2cb119-get-webhook-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_uuid` | path | `string` | yes | Webhook subscription UUID. |
