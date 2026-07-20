# Create Webhook with InsightIQ

Creates a new webhook in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Webhook](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Webhook event types to subscribe to. |
| `name` | body | `string` | yes | Friendly name for the webhook. |
| `url` | body | `string` | yes | Destination URL for webhook events. |
