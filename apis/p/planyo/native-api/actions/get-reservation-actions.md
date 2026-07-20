# Get Reservation Actions with Planyo

Retrieves reservation actions from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Get Reservation Actions](https://www.planyo.com/api.php?topic=get_reservation_actions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reservation_id` | query | `number` | no |
| `user_id` | query | `number` | no |
| `start_time` | query | `string` | no |
| `end_time` | query | `string` | no |
| `event_type` | query | `number` | no |
| `site_id` | query | `number` | no |
