# Update Webhook with Callingly

Updates a webhook in Callingly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/webhooks/{{webhookId}}`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Update Webhook](https://help.callingly.com/article/38-callingly-api-documentation#Update-a-Webhook-mvgYy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_direction` | body | `string` | no | The call direction filter. |
| `call_lead_status` | body | `string` | no | The call lead status filter. |
| `call_status` | body | `string` | no | The call status filter. |
| `event` | body | `string` | no | The webhook event type. |
| `field` | body | `string` | no | Only trigger when this lead field changes. |
| `filter` | body | `string` | no | Only trigger when the selected field matches this value. |
| `id` | body | `number` | yes | The Callingly webhook ID to update. |
| `name` | body | `string` | no | The webhook name. |
| `number_id` | body | `number` | no | The number ID filter. |
| `target_url` | body | `string` | no | The webhook destination URL. |
| `team_id` | body | `number` | no | The team ID filter. |
| `webhookId` | path | `number` | yes | The Callingly webhook ID to update in the path. |
