# Update Reservation Payment with Planyo

Updates a reservation payment in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Update Reservation Payment](https://www.planyo.com/api.php?topic=modify_reservation_payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payment_id` | query | `number` | yes |
| `reservation_id` | query | `number` | yes |
| `payment_status` | query | `number` | yes |
| `extra_info` | query | `string` | no |
