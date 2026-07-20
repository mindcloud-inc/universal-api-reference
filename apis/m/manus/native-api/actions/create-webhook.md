# Create Webhook with Manus

Creates a new webhook in Manus.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [Create Webhook](https://open.manus.ai/docs/v1/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook.url` | body | `string` | yes | Destination URL for webhook deliveries |
