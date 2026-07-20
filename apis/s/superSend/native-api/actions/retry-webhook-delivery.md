# Retry Webhook Delivery with SuperSend

Retries a webhook delivery in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/{id}/deliveries/{deliveryId}/retry`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Retry Webhook Delivery](https://docs.supersend.io/docs/webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `deliveryId` | path | `string` | yes |
| `team_id` | body | `string` | yes |
