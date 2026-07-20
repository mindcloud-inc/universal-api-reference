# Remove Reservation Payment with Planyo

Deletes a reservation payment from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Remove Reservation Payment](https://www.planyo.com/api.php?topic=remove_reservation_payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payment_id` | query | `number` | yes |
| `reservation_id` | query | `number` | yes |
