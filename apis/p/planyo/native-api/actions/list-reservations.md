# List Reservations with Planyo

Retrieves reservations from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [List Reservations](https://www.planyo.com/api.php?topic=list_reservations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_time` | query | `string` | yes |
| `end_time` | query | `string` | yes |
| `resource_id` | query | `number` | no |
| `detail_level` | query | `number` | no |
| `page` | query | `number` | no |
| `user_id` | query | `number` | no |
| `user_email` | query | `string` | no |
| `sort` | query | `string` | no |
| `sort_reverse` | query | `boolean` | no |
| `required_status` | query | `number` | no |
| `excluded_status` | query | `number` | no |
| `modified_since` | query | `string` | no |
| `list_by_creation_date` | query | `boolean` | no |
