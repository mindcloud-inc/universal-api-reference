# Do Reservation Action with Planyo

Performs a reservation action in Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Do Reservation Action](https://www.planyo.com/api.php?topic=do_reservation_action)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reservation_id` | query | `number` | yes |
| `action` | query | `string` | yes |
| `custom_data` | query | `string` | no |
| `comment` | query | `string` | no |
| `admin_id` | query | `number` | no |
| `is_quiet` | query | `boolean` | no |
