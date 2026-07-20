# Create Webhook with SMASHSEND Email Marketing

Creates a new webhook in SMASHSEND.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.smashsend.com`
- **Official documentation:** [Create Webhook](https://smashsend.com/docs/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Array of SMASHSEND event names that should trigger the webhook. |
| `token` | body | `string` | no | Optional shared secret token included in webhook deliveries. |
| `url` | body | `string` | yes | HTTPS endpoint that should receive SMASHSEND webhook events. |
