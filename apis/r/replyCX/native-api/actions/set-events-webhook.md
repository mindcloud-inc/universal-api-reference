# Set Events Webhook with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:account_id/webhook`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Set Events Webhook](https://help.reply.cx/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_url` | body | `string` | yes | — |
| `subscribed_events` | body | `list<object>` | yes | List of ReplyCX event subscriptions as objects with keys `key` and `is_subscribed`. |
| `is_enabled` | body | `boolean` | yes | — |
| `token` | body | `string` | yes | — |
