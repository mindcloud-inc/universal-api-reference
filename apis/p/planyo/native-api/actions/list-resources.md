# List Resources with Planyo

Retrieves resources from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [List Resources](https://www.planyo.com/api.php?topic=list_resources)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `detail_level` | query | `number` | no |
| `page` | query | `number` | no |
| `list_published_only` | query | `boolean` | no |
| `list_reservable_only` | query | `boolean` | no |
| `list_resource_types` | query | `string` | no |
| `admin_id` | query | `number` | no |
| `ppp_gps_coords_radius` | query | `number` | no |
| `ppp_resfilter` | query | `string` | no |
| `sort` | query | `string` | no |
| `site_id` | query | `number` | no |
