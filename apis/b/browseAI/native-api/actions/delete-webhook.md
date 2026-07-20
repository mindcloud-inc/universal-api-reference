# Delete Webhook with Browse AI

Deletes a webhook from Browse AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/robots/:robotId/webhooks/:webhookId`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Delete Webhook](https://developers.browse.ai/v2#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `webhookId` | path | `string` | yes | Unique webhookId ID |
