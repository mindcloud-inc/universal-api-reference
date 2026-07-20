# Update Webhook with InsightIQ

Updates an existing webhook in InsightIQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/webhooks/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Webhook](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Webhook event types to subscribe to. |
| `id` | path | `string` | yes | InsightIQ webhook identifier. |
| `is_active` | body | `boolean` | no | Whether the webhook should remain active. |
| `name` | body | `string` | yes | Friendly name for the webhook. |
| `url` | body | `string` | yes | Destination URL for webhook events. |
