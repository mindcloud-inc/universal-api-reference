# Delete Webhook with Voog

Deletes an existing webhook from the current Voog site.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Delete Webhook](https://www.voog.com/developers/api/resources/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `number` | yes | Numeric webhook ID. |
