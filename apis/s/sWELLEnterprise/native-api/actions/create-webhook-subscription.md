# Create Webhook Subscription with SWELLEnterprise

Creates a webhook subscription in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/subscriptions`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Webhook Subscription](https://dashboard.swellsystem.com/docs#webhooks-POSTapi-v1-webhooks-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The webhook name. |
| `url` | body | `string` | yes | The webhook URL. |
| `events[]` | body | `array<string>` | yes | Array of event types. |
| `headers` | body | `object` | no | Custom headers to send. |
| `max_retries` | body | `number` | no | Maximum retry attempts. |
| `timeout` | body | `number` | no | Request timeout in seconds. |
