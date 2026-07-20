# Find Equipment with Encircle

Retrieves equipment from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/equipment`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Equipment](https://encircleinc.github.io/public-api/#/paths/~1v2~1equipment/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | no | — |
| `is_retired` | query | `boolean` | no | — |
| `equipment_type` | query | `list` | no | Accepted values: `air_mover`, `air_scrubber`, `dehumidifier`, `dryer`, `heater`, `other`. |
| `currently_placed_in_claim_id` | query | `number` | no | — |
| `order` | query | `list` | no | Accepted values: `newest`, `oldest`. |
| `limit` | query | `number` | no | — |
| `after` | query | `string` | no | — |
