# Find Property Claims with Encircle

Retrieves property claims from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_claims`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Property Claims](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignment_identifier` | query | `string` | no | — |
| `contractor_identifier` | query | `string` | no | — |
| `insurer_identifier` | query | `string` | no | — |
| `policyholder_name` | query | `string` | no | — |
| `order` | query | `list` | no | Accepted values: `newest`, `oldest`. |
| `limit` | query | `number` | no | — |
| `after` | query | `string` | no | — |
