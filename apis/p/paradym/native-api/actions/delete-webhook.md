# Delete Webhook with Paradym

Deletes an existing webhook from Paradym.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/webhooks/:webhookId`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Delete Webhook](https://paradym.id/reference#tag/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The webhook subscription ID. |
