# Update Webhook with MailerSend

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:webhook_id`
- **Base URL:** `https://api.mailersend.com/v1`
- **Official documentation:** [Update Webhook](https://developers.mailersend.com/api/v1/webhooks#update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | ID of the webhook to update. |
| `name` | body | `string` | no | Updated webhook name. |
| `url` | body | `string` | no | Updated destination URL for the webhook. |
| `events[]` | body | `array<string>` | no | Updated MailerSend event types for the webhook. |
| `enabled` | body | `boolean` | no | Whether the webhook should be active after update. |
