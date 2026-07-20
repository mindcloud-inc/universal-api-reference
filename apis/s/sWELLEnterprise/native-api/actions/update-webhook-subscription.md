# Update Webhook Subscription with SWELLEnterprise

Updates a webhook subscription in SWELLEnterprise.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/subscriptions/:id`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Update Webhook Subscription](https://dashboard.swellsystem.com/docs#webhooks-PUTapi-v1-webhooks-subscriptions--id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The webhook subscription ID. |
| `name` | body | `string` | no | The webhook name. |
| `url` | body | `string` | no | The webhook URL. |
| `events[]` | body | `array<string>` | no | Array of event types. |
| `is_active` | body | `boolean` | no | Whether the webhook is active. |
| `headers` | body | `object` | no | Custom headers. |
| `max_retries` | body | `number` | no | Maximum retry attempts. |
| `timeout` | body | `number` | no | Request timeout. |
