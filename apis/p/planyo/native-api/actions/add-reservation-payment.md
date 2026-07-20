# Add Reservation Payment with Planyo

Adds a reservation payment in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Add Reservation Payment](https://www.planyo.com/api.php?topic=add_reservation_payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reservation_id` | query | `number` | yes |
| `payment_mode` | query | `number` | yes |
| `payment_status` | query | `number` | yes |
| `transaction_id` | query | `string` | yes |
| `amount` | query | `number` | yes |
| `currency` | query | `string` | yes |
| `payment_time` | query | `string` | no |
| `extra_info` | query | `string` | no |
| `is_quiet` | query | `boolean` | no |
| `payment_response_code` | query | `string` | no |
| `transaction_status_text` | query | `string` | no |
