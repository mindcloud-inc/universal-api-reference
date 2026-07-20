# Delete Reservation with Planyo

Deletes an existing reservation from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Delete Reservation](https://www.planyo.com/api.php?topic=delete_reservation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reservation_id` | query | `number` | yes |
| `delete_user_without_reservations` | query | `boolean` | no |
