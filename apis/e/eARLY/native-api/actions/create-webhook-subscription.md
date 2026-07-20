# Create Webhook Subscription with EARLY

Creates a webhook subscription in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/webhooks/subscription`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Webhook Subscription](https://developers.early.app/#1f0ca463-6396-4be9-b62e-fa60d274e1ff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Webhook event name. |
| `target_url` | body | `string` | yes | Webhook delivery URL. |
