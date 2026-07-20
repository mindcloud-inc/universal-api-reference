# Update Reservation with Planyo

Updates an existing reservation in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Update Reservation](https://www.planyo.com/api.php?topic=modify_reservation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reservation_id` | query | `number` | yes |
| `start_time` | query | `string` | no |
| `end_time` | query | `string` | no |
| `resource_id` | query | `number` | no |
| `quantity` | query | `number` | no |
| `admin_mode` | query | `boolean` | no |
| `send_notifications` | query | `boolean` | no |
| `recalculate_price` | query | `boolean` | no |
| `comments` | query | `string` | no |
| `user_id` | query | `number` | no |
| `assignment1` | query | `string` | no |
