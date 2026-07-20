# Create Webhook with Cryptlex

Creates a webhook in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/webhooks`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Create Webhook](https://api.cryptlex.com/v3/docs#tag/Webhooks/operation/post/v3/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Whether the webhook is enabled. |
| `events[]` | body | `array<string>` | yes | Events to subscribe the webhook to. Send multiple values as a array. |
| `name` | body | `string` | yes | Webhook name. |
| `token` | body | `string` | yes | Shared secret token for webhook verification. |
| `url` | body | `string` | yes | Destination URL for the webhook. |
