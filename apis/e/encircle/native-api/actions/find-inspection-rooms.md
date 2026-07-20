# Find Inspection Rooms with Encircle

Retrieves inspection rooms from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_inspections/:property_inspection_id/structures/:structure_id/rooms`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Inspection Rooms](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}~1structures~1{structure_id}~1rooms/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_inspection_id` | path | `number` | yes | — |
| `structure_id` | path | `number` | yes | — |
| `order` | query | `list` | no | Accepted values: `newest`, `oldest`. |
| `limit` | query | `number` | no | — |
| `after` | query | `string` | no | — |
