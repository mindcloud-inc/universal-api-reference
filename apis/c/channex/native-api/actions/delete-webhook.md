# Delete Webhook with Channex

Deletes an existing webhook from Channex.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Delete Webhook](https://docs.channex.io/api-v.1-documentation/webhook-collection#remove-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the webhook to delete. |
