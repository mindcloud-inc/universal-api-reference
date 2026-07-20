# Create Webhook with MailSlurp Email Plugin

Creates a new webhook in MailSlurp.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inboxId/webhooks`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Create Webhook](https://api.mailslurp.com/swagger-ui/index.html#/WebhookController/createWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | no | The MailSlurp inbox ID that will own the webhook. |
