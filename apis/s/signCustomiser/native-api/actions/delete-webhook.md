# Delete Webhook with Sign Customiser

Deletes an existing webhook subscription from Sign Customiser.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/webhooks/:webhookId`
- **Base URL:** `https://web.signcustomiser.com`
- **Official documentation:** [Delete Webhook](https://www.signcustomiser.com/help/api/delete-delete-a-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `number` | yes | The ID of the webhook. |
