# Get Rental Price with Planyo

Retrieves a rental price from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Get Rental Price](https://www.planyo.com/api.php?topic=get_rental_price)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_id` | query | `number` | yes |
| `start_time` | query | `string` | yes |
| `end_time` | query | `string` | yes |
| `quantity` | query | `number` | yes |
| `admin_mode` | query | `boolean` | no |
| `shopping_cart_position` | query | `number` | no |
| `shopping_cart_resource_quantity` | query | `number` | no |
| `shopping_cart_resource_hours` | query | `number` | no |
| `shopping_cart_total_price` | query | `number` | no |
| `wants_share` | query | `string` | no |
| `user_id` | query | `number` | no |
| `user_email` | query | `string` | no |
