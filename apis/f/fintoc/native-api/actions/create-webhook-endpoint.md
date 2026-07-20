# Create Webhook Endpoint with Fintoc

Creates a webhook endpoint in Fintoc.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhook_endpoints`
- **Base URL:** `https://api.fintoc.com`
- **Official documentation:** [Create Webhook Endpoint](https://docs.fintoc.com/reference/webhook-endpoints-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public HTTPS endpoint that receives Fintoc webhooks. |
| `enabled_events` | body | `object` | yes | Enabled webhook events array as JSON. |
