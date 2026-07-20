# Delete Webhook with Weavely

Deletes a webhook from a Weavely form.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/webhooks/:webhookId`
- **Base URL:** `https://api.weavely.ai/v1`
- **Official documentation:** [Delete Webhook](https://help.weavely.ai/developers/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The ID of the form where the webhook is registered. |
| `webhookId` | path | `string` | yes | The ID of the webhook to delete. |
