# Subscribe to Webhook with Drag'n Survey

Creates a webhook subscription in Drag'n Survey.

## Endpoint

- **Method:** `POST`
- **Path:** `webhooks`
- **Base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`
- **Official documentation:** [Subscribe to Webhook](https://developer.dragnsurvey.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | Element type that should trigger the webhook. |
| `element_id` | body | `string` | yes | Element id that should trigger the webhook. |
| `event_type` | body | `string` | yes | Webhook event to subscribe to. |
| `url` | body | `string` | yes | Secure endpoint that should receive the webhook call. |
