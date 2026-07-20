# Update Webhook with Channex

Updates an existing webhook in Channex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Webhook](https://docs.channex.io/api-v.1-documentation/webhook-collection#update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the webhook to update. |
| `webhook` | body | `object` | yes | Top-level webhook payload object documented by Channex for webhook updates. |
