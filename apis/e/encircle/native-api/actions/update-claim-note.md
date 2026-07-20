# Update Claim Note with Encircle

Updates a claim note in Encircle.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/property_claims/:property_claim_id/notes/:note_id`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Update Claim Note](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes~1{note_id}/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes |
| `note_id` | path | `number` | yes |
| `title` | body | `string` | no |
| `text` | body | `string` | no |
