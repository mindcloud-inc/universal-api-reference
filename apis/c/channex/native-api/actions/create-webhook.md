# Create Webhook with Channex

Creates a new webhook in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Create Webhook](https://docs.channex.io/api-v.1-documentation/webhook-collection#create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook` | body | `object` | yes | Top-level webhook payload object documented by Channex for webhook creation. |
