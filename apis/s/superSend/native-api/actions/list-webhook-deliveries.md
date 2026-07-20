# List Webhook Deliveries with SuperSend

Retrieves webhook deliveries from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/{id}/deliveries`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Webhook Deliveries](https://docs.supersend.io/docs/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `team_id` | query | `string` | yes | — |
| `status` | query | `string` | no | Allowed values: pending, delivered, failed, retrying. |
| `event_type` | query | `string` | no | — |
| `campaign_id` | query | `string` | no | — |
| `search` | query | `string` | no | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
