# Update Webhook with Grist

Updates an existing webhook in a Grist document.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/docs/:docId/webhooks/:webhookId`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Update Webhook](https://support.getgrist.com/api/#tag/webhooks/operation/modifyWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `webhookId` | path | `string` | yes | Webhook ID |
| `webhook` | body | `string` | yes | Webhook patch payload as JSON |
