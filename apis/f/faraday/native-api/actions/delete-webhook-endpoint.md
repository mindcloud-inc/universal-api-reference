# Delete Webhook Endpoint with Faraday

Deletes an existing webhook endpoint from Faraday.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhook_endpoints/:webhook_endpoint_id`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Delete Webhook Endpoint](https://faraday.ai/docs/reference/deletewebhookendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_endpoint_id` | path | `string` | no | Faraday webhook endpoint ID. |
