# Delete Webhook with Grist

Deletes a webhook from a Grist document.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/docs/:docId/webhooks/:webhookId`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Delete Webhook](https://support.getgrist.com/api/#tag/webhooks/operation/deleteWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `webhookId` | path | `string` | yes | Webhook ID |
