# List Alerts with Chargback

Retrieves chargeback alert records from Chargback.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v1/alerts/`
- **Base URL:** `https://api.chargeback.io`
- **Official documentation:** [List Alerts](https://api.chargeback.io/api/public/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `page_size` | query | `number` | no |
| `ordered_by` | query | `string` | no |
| `alert_status` | query | `string` | no |
| `alert_service` | query | `string` | no |
| `business_account` | query | `string` | no |
