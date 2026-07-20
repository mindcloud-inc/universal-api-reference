# Create Webhook Endpoint with SureCart

## Endpoint

- **Method:** `POST`
- **Path:** `v1/webhook_endpoints`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Create Webhook Endpoint](https://developer.surecart.com/api-reference/webhook-endpoints/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_endpoint.url` | body | `string` | yes | The public URL for this webhook endpoint. |
| `webhook_endpoint.description` | body | `string` | no | Optional description for the webhook endpoint. |
