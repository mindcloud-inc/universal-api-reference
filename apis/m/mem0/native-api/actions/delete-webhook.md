# Delete Webhook with Mem0

Deletes an existing webhook from Mem0.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/webhooks/:webhook_id/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Delete Webhook](https://docs.mem0.ai/api-reference/webhook/delete-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Mem0 webhook ID from the webhook resource path. |
