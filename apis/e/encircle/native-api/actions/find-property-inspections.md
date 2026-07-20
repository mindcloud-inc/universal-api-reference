# Find Property Inspections with Encircle

Retrieves property inspections from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_inspections`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Property Inspections](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `list` | no | Accepted values: `newest`, `oldest`. |
| `limit` | query | `number` | no | — |
| `after` | query | `string` | no | — |
