# Update Webhook with Webex

Updates an existing webhook in Webex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Update Webhook](https://developer.webex.com/messaging/docs/api/v1/webhooks/update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | Webhook identifier. |
| `name` | body | `string` | yes | Updated webhook display name. |
| `targetUrl` | body | `string` | yes | Updated HTTPS endpoint that receives webhook events. |
| `resource` | body | `string` | yes | Webhook resource type. |
| `event` | body | `string` | yes | Webhook event type. |
