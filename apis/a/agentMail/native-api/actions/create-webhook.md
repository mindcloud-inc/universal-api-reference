# Create Webhook with Agent Mail

Creates a new webhook in AgentMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Create Webhook](https://docs.agentmail.to/api-reference/webhooks/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | no | Client-provided idempotency ID. |
| `event_types[]` | body | `array<string>` | yes | Webhook event types to subscribe to. Send multiple values as a array. |
| `inbox_ids[]` | body | `array<string>` | no | Inbox IDs to subscribe to the webhook. Send multiple values as a array. |
| `pod_ids[]` | body | `array<string>` | no | Pod IDs to subscribe to the webhook. Send multiple values as a array. |
| `url` | body | `string` | yes | Webhook destination URL. |
