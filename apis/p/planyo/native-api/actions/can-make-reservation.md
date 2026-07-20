# Can Make Reservation with Planyo

Checks whether a reservation can be made in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Can Make Reservation](https://www.planyo.com/api.php?topic=can_make_reservation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_id` | query | `number` | yes |
| `start_time` | query | `string` | yes |
| `end_time` | query | `string` | yes |
| `quantity` | query | `number` | yes |
| `assignment1` | query | `string` | no |
| `admin_mode` | query | `boolean` | no |
| `wants_share` | query | `string` | no |
| `user_id` | query | `number` | no |
| `user_email` | query | `string` | no |
| `excluded_reservation_id` | query | `number` | no |
| `return_availability` | query | `boolean` | no |
| `return_price` | query | `string` | no |
