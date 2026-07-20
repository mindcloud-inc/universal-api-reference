# Get Webhook with Channex

Retrieves an existing webhook from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Get Webhook](https://docs.channex.io/api-v.1-documentation/webhook-collection#get-webhook-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the webhook to retrieve. |
