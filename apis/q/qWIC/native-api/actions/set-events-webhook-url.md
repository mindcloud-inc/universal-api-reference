# Set Events Webhook URL with QWIC

Updates the events webhook URL in QWIC.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:account_id/webhook`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Set Events Webhook URL](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#set-webhook-url-for-events-feature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | The account ID. |
| `webhook_url` | body | `string` | yes | The webhook endpoint URL. |
| `subscribed_events[]` | body | `array<object>` | yes | The subscribed event objects. |
| `is_enabled` | body | `boolean` | yes | Whether the webhook is enabled. |
| `token` | body | `string` | yes | The webhook verification token. |
