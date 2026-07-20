# Find Property By Entity with Rachio Smart Hose Timer

Finds a property in Rachio by entity ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/property/findPropertyByEntity`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Find Property By Entity](https://rachio.readme.io/reference/propertyservice_findpropertybyentity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id.base_station_id` | query | `string` | no | Smart Hose Timer base station UUID. Provide only one entity selector. |
| `resource_id.lighting_area_id` | query | `string` | no | Lighting area UUID. Provide only one entity selector. |
| `resource_id.location_id` | query | `string` | no | Location entity UUID. Provide only one entity selector. |
