# Create Webhook Subscription with Chargback

Creates a new webhook subscription in Chargback.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhook/subscriptions/`
- **Base URL:** `https://api.chargeback.io`
- **Official documentation:** [Create Webhook Subscription](https://api.chargeback.io/api/public/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_type` | body | `string` | yes |
| `callback_url` | body | `string` | yes |
