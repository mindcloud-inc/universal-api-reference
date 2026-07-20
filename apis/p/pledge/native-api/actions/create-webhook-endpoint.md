# Create Webhook Endpoint with Pledge

Creates a webhook endpoint in Pledge.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Create Webhook Endpoint](https://developer.pledge.to/api/#tag/Webhook%20Endpoints/operation/createWebhookEndpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL to notify when subscribed events occur. |
