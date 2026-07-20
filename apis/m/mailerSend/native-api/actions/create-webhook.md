# Create Webhook with MailerSend

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.mailersend.com/v1`
- **Official documentation:** [Create Webhook](https://developers.mailersend.com/api/v1/webhooks#create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | body | `string` | yes | ID of the MailerSend domain that should emit webhook events. |
| `name` | body | `string` | yes | Human-readable name for the webhook. |
| `url` | body | `string` | yes | Destination URL that should receive MailerSend webhook calls. |
| `events[]` | body | `array<string>` | yes | MailerSend event types that should trigger this webhook. |
| `enabled` | body | `boolean` | no | Whether the webhook should be active after creation. |
