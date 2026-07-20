# Assign User To Claim with Encircle

Assigns a user to a property claim in Encircle.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/property_claims/:property_claim_id/assignments`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Assign User To Claim](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1assignments/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes |
| `id` | body | `string` | yes |
