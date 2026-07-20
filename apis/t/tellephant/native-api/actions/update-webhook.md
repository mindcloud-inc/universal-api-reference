# Update webhook with Tellephant

Updates a webhook configuration in Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.tellephant.com/api/v2/user/webhook/update`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Update webhook](https://app.tellephant.com/api-documentation#update-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_type` | body | `list` | yes | Webhook type to update: delivery_response or incoming_message. Accepted values: `delivery_response`, `incoming_message`. |
| `webhook_endpoint` | body | `string` | yes | Webhook destination URL. |
| `webhook_status` | body | `boolean` | yes | Whether the webhook is enabled. |
