# Update Webhook with Agent Mail

Updates an existing webhook in AgentMail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/{webhook_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Update Webhook](https://docs.agentmail.to/api-reference/webhooks/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `add_inbox_ids[]` | body | `array<string>` | no | Inbox IDs to subscribe to the webhook. Send multiple values as a array. |
| `add_pod_ids[]` | body | `array<string>` | no | Pod IDs to subscribe to the webhook. Send multiple values as a array. |
| `remove_inbox_ids[]` | body | `array<string>` | no | Inbox IDs to unsubscribe from the webhook. Send multiple values as a array. |
| `remove_pod_ids[]` | body | `array<string>` | no | Pod IDs to unsubscribe from the webhook. Send multiple values as a array. |
| `webhook_id` | path | `string` | yes | The AgentMail webhook ID. |
