# Find Inspection Structures with Encircle

Retrieves inspection structures from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_inspections/:property_inspection_id/structures`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Inspection Structures](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}~1structures/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_inspection_id` | path | `number` | yes | — |
| `order` | query | `list` | no | Accepted values: `newest`, `oldest`. |
| `limit` | query | `number` | no | — |
| `after` | query | `string` | no | — |
