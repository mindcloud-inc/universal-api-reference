# Delete Webhook with Figma

Deletes an existing webhook from Figma.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.figma.com/v2/webhooks/:webhook_id`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Delete Webhook](https://developers.figma.com/docs/rest-api/webhooks-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Webhook identifier to delete. |
