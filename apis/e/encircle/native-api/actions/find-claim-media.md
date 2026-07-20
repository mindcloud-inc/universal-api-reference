# Find Claim Media with Encircle

Retrieves claim media from Encircle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_claims/:property_claim_id/media`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Find Claim Media](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1media/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes |
| `limit` | query | `number` | no |
| `after` | query | `string` | no |
