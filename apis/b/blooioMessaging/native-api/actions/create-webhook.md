# Create Webhook with Blooio Messaging

Creates a new webhook in Blooio Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Create Webhook](https://docs.blooio.com/webhooks/createWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `string` | no | Webhook events to subscribe to. |
| `webhook_url` | body | `string` | yes | Webhook callback URL. |
