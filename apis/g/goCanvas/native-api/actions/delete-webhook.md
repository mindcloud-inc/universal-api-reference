# Delete Webhook with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/webhooks/:webhookId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Webhook](https://api.gocanvas.com/api/v3/docs#delete-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `webhookId` | path | `number` | yes | — |
| `hard_delete` | query | `boolean` | no | Permanently deletes the webhook when true; omitted defaults to soft delete. |
