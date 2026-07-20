# List Payments with Planyo

Retrieves payments from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [List Payments](https://www.planyo.com/api.php?topic=list_payments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | query | `string` | yes |
| `end_date` | query | `string` | yes |
| `resource_id` | query | `number` | no |
| `site_id` | query | `number` | no |
| `payment_mode_id_filter` | query | `number` | no |
| `status` | query | `number` | no |
