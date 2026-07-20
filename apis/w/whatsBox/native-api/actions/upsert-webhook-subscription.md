# Upsert Webhook Subscription with WhatsBox

Creates or updates a webhook subscription in WhatsBox.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook-subscriptions`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Upsert Webhook Subscription](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | body | `string` | yes | Channel ID for the WhatsApp number. |
| `subscriber_reference_id` | body | `string` | yes | Subscriber reference ID for the webhook. |
| `webhook_url` | body | `string` | yes | Destination URL for webhook delivery. |
| `platform` | body | `string` | yes | Platform label for the webhook subscription. |
