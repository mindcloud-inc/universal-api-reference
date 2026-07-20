# Update Webhook with folk

Updates an existing webhook in folk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/webhooks/:webhookId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Update Webhook](https://developer.folk.app/api-reference/webhooks/update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The ID of the webhook to update. |
| `name` | body | `string` | no | The updated friendly name for the webhook. |
| `targetUrl` | body | `string` | no | The updated public URL that receives webhook deliveries. |
| `subscribedEvents[0].eventType` | body | `string` | no | The updated first subscribed webhook event type. |
| `subscribedEvents[0].filter.groupId` | body | `string` | no | Optionally update the first subscribed event filter to a specific Folk group ID. |
