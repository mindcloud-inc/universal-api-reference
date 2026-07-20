# Find Claim Notes with Encircle

Retrieves claim notes from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_claims/:property_claim_id/notes`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Claim Notes](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes | — |
| `order` | query | `list` | no | Accepted values: `newest`, `oldest`. |
| `limit` | query | `number` | no | — |
| `after` | query | `string` | no | — |
