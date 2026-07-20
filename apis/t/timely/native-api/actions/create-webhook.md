# Create Webhook with Timely

Creates a webhook in Timely.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.1/{account_id}/webhooks`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Create Webhook](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `webhook.url` | body | `string` | yes | URL to send webhook payloads to (must be HTTPS) |
| `webhook.subscriptions[]` | body | `array<string>` | yes | List of event types to subscribe to |
| `webhook.secret_token` | body | `string` | no | Secret token used to sign webhook payloads. The signature will be included in the X-Signature header. |
| `webhook.active` | body | `string` | no | Whether the webhook is active. Defaults to true. |
| `webhook.custom_headers` | body | `string` | no | Custom HTTP headers to include in webhook requests |
