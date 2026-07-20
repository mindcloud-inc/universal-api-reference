# Update Webhook Endpoint with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/webhook_endpoints/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Webhook Endpoint](https://developer.surecart.com/api-reference/webhook-endpoints/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The webhook endpoint ID to update. |
| `webhook_endpoint.description` | body | `string` | yes | Updated description for the webhook endpoint. |
