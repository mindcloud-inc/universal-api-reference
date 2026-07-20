# Create Claim Note with Encircle

Creates a claim note in Encircle.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/property_claims/:property_claim_id/notes`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Create Claim Note](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes |
| `title` | body | `string` | yes |
| `text` | body | `string` | no |
