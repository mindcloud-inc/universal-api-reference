# Create Webhook with MailerLite

Creates a new webhook in MailerLite.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Create Webhook](https://developers.mailerlite.com/docs/webhooks#create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Friendly name for the webhook. |
| `events[]` | body | `array<string>` | yes | Webhook events to subscribe to. |
| `url` | body | `string` | yes | Destination URL for MailerLite webhook deliveries. |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled immediately after creation. |
| `batchable` | body | `boolean` | no | Whether MailerLite can batch event deliveries for this webhook. |
