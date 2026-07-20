# List Domains with SuperSend

Retrieves domains from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Domains](https://docs.supersend.io/docs/managed-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | query | `string` | no | — |
| `status` | query | `string` | no | Allowed values: pending, purchasing, purchased, setting_up, active, purchase_failed, setup_failed, inactive, expired, cancelled. |
| `managed` | query | `string` | no | Allowed values: internal, external. |
| `search` | query | `string` | no | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
