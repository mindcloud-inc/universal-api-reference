# Create Reservation with Planyo

Creates a new reservation in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Create Reservation](https://www.planyo.com/api.php?topic=make_reservation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_id` | query | `number` | yes |
| `start_time` | query | `string` | yes |
| `end_time` | query | `string` | yes |
| `quantity` | query | `number` | yes |
| `email` | query | `string` | yes |
| `first_name` | query | `string` | yes |
| `last_name` | query | `string` | no |
| `admin_mode` | query | `boolean` | no |
| `send_notifications` | query | `boolean` | no |
| `force_status` | query | `number` | no |
| `wants_share` | query | `string` | no |
| `user_id` | query | `number` | no |
| `user_notes` | query | `string` | no |
| `admin_notes` | query | `string` | no |
| `assignment1` | query | `string` | no |
| `add_to_waitlist` | query | `boolean` | no |
