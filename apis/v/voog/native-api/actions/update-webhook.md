# Update Webhook with Voog

Updates an existing webhook in the current Voog site.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Update Webhook](https://www.voog.com/developers/api/resources/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Whether the webhook is enabled. |
| `event` | body | `string` | yes | Webhook event name. |
| `target` | body | `string` | yes | Webhook target object. |
| `url` | body | `string` | yes | Destination URL for webhook delivery. |
| `webhookId` | path | `number` | yes | Numeric webhook ID. |
