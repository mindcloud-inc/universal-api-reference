# Get Claim Note with Encircle

Retrieves a claim note from Encircle by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/property_claims/:property_claim_id/notes/:note_id`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Get Claim Note](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes~1{note_id}/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes |
| `note_id` | path | `number` | yes |
