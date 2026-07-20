# Unassign User From Claim with Encircle

Unassigns a user from a property claim in Encircle.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/property_claims/:property_claim_id/assignments`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Unassign User From Claim](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1assignments/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes |
| `id` | body | `string` | yes |
