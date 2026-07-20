# Subscribe an Event with WaiverForever

Creates a webhook subscription in WaiverForever.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v1/webhooks/`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Subscribe an Event](https://docs.waiverforever.com/#subscribe-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Webhook event name to subscribe to. |
| `target_url` | body | `string` | yes | Callback URL that receives webhook events. |
| `template_id` | body | `string` | yes | Template to subscribe against. |
