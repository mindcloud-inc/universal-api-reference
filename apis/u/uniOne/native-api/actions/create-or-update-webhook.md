# Create Or Update Webhook with UniOne

Creates or updates a webhook in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `webhook/set.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Create Or Update Webhook](https://docs.unione.io/en/web-api-ref#webhook-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook endpoint URL. |
| `status` | body | `string` | no | Webhook status. |
| `event_format` | body | `string` | no | Webhook event payload format. |
| `delivery_info` | body | `number` | no | Whether to include delivery details. |
| `single_event` | body | `number` | no | Whether to send one event per callback. |
| `max_parallel` | body | `number` | no | Maximum parallel webhook deliveries. |
| `events.spam_block` | body | `string` | no | Spam block events to subscribe to. Send multiple values as a array. |
| `events.email_status` | body | `string` | no | Email status events to subscribe to. Send multiple values as a array. |
