# Get Webhook Delivery with SuperSend

Retrieves a webhook delivery from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/{id}/deliveries/{deliveryId}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Get Webhook Delivery](https://docs.supersend.io/docs/webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `deliveryId` | path | `string` | yes |
| `team_id` | query | `string` | yes |
