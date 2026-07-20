# List Users with Planyo

Retrieves users from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [List Users](https://www.planyo.com/api.php?topic=list_users)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `site_id` | query | `number` | no |
| `detail_level` | query | `number` | no |
| `email` | query | `string` | no |
| `first_name` | query | `string` | no |
| `last_name` | query | `string` | no |
| `list_created_by_admin` | query | `boolean` | no |
| `list_unconfirmed` | query | `boolean` | no |
