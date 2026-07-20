# List Lighting Zones with Rachio Smart Lighting Controller

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/lighting/listLightingZones`
- **Base URL:** `https://cloud-rest.rach.io`
- **Official documentation:** [List Lighting Zones](https://rachio.readme.io/reference/lightingservice_listlightingzones)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lighting_area_id` | query | `string` | no | Limit results to a lighting area. |
| `lighting_controller_id` | query | `string` | no | Limit results to a lighting controller. |
| `lighting_scene_id` | query | `string` | no | Limit results to a lighting scene. |
| `lighting_zone_group_id` | query | `string` | no | Limit results to a lighting zone group. |
