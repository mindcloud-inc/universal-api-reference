# Create Webhook with Grist

Creates a new webhook in a Grist document.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/webhooks`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Create Webhook](https://support.getgrist.com/api/#tag/webhooks/operation/createWebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `webhooks` | body | `string` | yes | JSON array of webhook objects with fields: name url enabled eventTypes tableId |
