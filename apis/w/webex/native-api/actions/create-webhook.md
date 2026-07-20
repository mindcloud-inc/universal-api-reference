# Create Webhook with Webex

Creates a new webhook in Webex.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Create Webhook](https://developer.webex.com/messaging/docs/api/v1/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Webhook display name. |
| `targetUrl` | body | `string` | yes | HTTPS endpoint that receives webhook events. |
| `resource` | body | `string` | yes | Webhook resource type. |
| `event` | body | `string` | yes | Webhook event type. |
