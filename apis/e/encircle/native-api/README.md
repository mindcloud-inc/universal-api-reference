# Encircle: Native API Reference

A consolidated summary of Encircle's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://encircleinc.github.io/public-api/
- **OpenAPI specification:** https://api.encircleapp.com/openapi_v3.json
- **API base URL:** `https://api.encircleapp.com`

## Authentication

### Bearer Token

Use an Encircle bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.encircleapp.com/hc/en-us/articles/360051960511-Bearer-Token)

## API conventions

Responses from this API use JSON. Response data is read from `list`. The next-page cursor is read from `cursor.after`.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `after` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign User To Claim](actions/assign-user-to-claim.md) | `POST /v1/property_claims/:property_claim_id/assignments` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1assignments/post) |
| [Create Claim Note](actions/create-claim-note.md) | `POST /v1/property_claims/:property_claim_id/notes` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes/post) |
| [Create Property Claim](actions/create-property-claim.md) | `POST /v1/property_claims` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims/post) |
| [Create Property Inspection](actions/create-property-inspection.md) | `POST /v1/property_inspections` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections/post) |
| [Find Claim Assignments](actions/find-claim-assignments.md) | `GET /v1/property_claims/:property_claim_id/assignments` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1assignments/get) |
| [Find Claim Media](actions/find-claim-media.md) | `GET /v1/property_claims/:property_claim_id/media` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1media/get) |
| [Find Claim Notes](actions/find-claim-notes.md) | `GET /v1/property_claims/:property_claim_id/notes` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes/get) |
| [Find Claim Rooms](actions/find-claim-rooms.md) | `GET /v1/property_claims/:property_claim_id/structures/:structure_id/rooms` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1structures~1{structure_id}~1rooms/get) |
| [Find Claim Structures](actions/find-claim-structures.md) | `GET /v1/property_claims/:property_claim_id/structures` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1structures/get) |
| [Find Equipment](actions/find-equipment.md) | `GET /v2/equipment` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v2~1equipment/get) |
| [Find Inspection Assignments](actions/find-inspection-assignments.md) | `GET /v1/property_inspections/:property_inspection_id/assignments` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}~1assignments/get) |
| [Find Inspection Rooms](actions/find-inspection-rooms.md) | `GET /v1/property_inspections/:property_inspection_id/structures/:structure_id/rooms` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}~1structures~1{structure_id}~1rooms/get) |
| [Find Inspection Structures](actions/find-inspection-structures.md) | `GET /v1/property_inspections/:property_inspection_id/structures` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}~1structures/get) |
| [Find Organization Brands](actions/find-organization-brands.md) | `GET /v1/organizations/:organization_id/brands` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1organizations~1{organization_id}~1brands/get) |
| [Find Organizations](actions/find-organizations.md) | `GET /v1/organizations` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1organizations/get) |
| [Find Property Claims](actions/find-property-claims.md) | `GET /v1/property_claims` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims/get) |
| [Find Property Inspections](actions/find-property-inspections.md) | `GET /v1/property_inspections` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections/get) |
| [Get Claim Note](actions/get-claim-note.md) | `GET /v1/property_claims/:property_claim_id/notes/:note_id` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes~1{note_id}/get) |
| [Get Property Claim](actions/get-property-claim.md) | `GET /v1/property_claims/:property_claim_id` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}/get) |
| [Get Property Inspection](actions/get-property-inspection.md) | `GET /v1/property_inspections/:property_inspection_id` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}/get) |
| [Unassign User From Claim](actions/unassign-user-from-claim.md) | `DELETE /v1/property_claims/:property_claim_id/assignments` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1assignments/delete) |
| [Update Claim Note](actions/update-claim-note.md) | `PATCH /v1/property_claims/:property_claim_id/notes/:note_id` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}~1notes~1{note_id}/patch) |
| [Update Property Claim](actions/update-property-claim.md) | `PATCH /v1/property_claims/:property_claim_id` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}/patch) |
| [Update Property Inspection](actions/update-property-inspection.md) | `PATCH /v1/property_inspections/:property_inspection_id` | [docs](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}/patch) |
