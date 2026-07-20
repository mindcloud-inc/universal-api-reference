# <img src="https://images.mindcloud.co/apps/icons/encircle_1773839659950.png" alt="Encircle logo" width="28" height="28"> Encircle: Universal API

Document claims, inspections, equipment, and restoration field data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encircle/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getencircle.com
- **Vendor API docs:** https://encircleinc.github.io/public-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Claim Assignments](actions/find-claim-assignments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-assignments?connectionId=$CONNECTION_ID&propertyClaimId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Find Equipment](actions/find-equipment.md) | GET | Retrieves equipment from Encircle. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Find Claim Media](actions/find-claim-media.md) | GET | Retrieves claim media from Encircle. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Claim Note](actions/create-claim-note.md) | POST | Creates a claim note in Encircle. |
| [Find Claim Notes](actions/find-claim-notes.md) | GET | Retrieves claim notes from Encircle. |
| [Get Claim Note](actions/get-claim-note.md) | GET | Retrieves a claim note from Encircle by ID. |
| [Update Claim Note](actions/update-claim-note.md) | PUT | Updates a claim note in Encircle. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Find Organizations](actions/find-organizations.md) | GET | Retrieves organizations from Encircle. |

### Organization Brand

| Action | Method | Description |
| --- | --- | --- |
| [Find Organization Brands](actions/find-organization-brands.md) | GET | Retrieves organization brands from Encircle. |

### Property Claim

| Action | Method | Description |
| --- | --- | --- |
| [Create Property Claim](actions/create-property-claim.md) | POST | Creates a property claim in Encircle. |
| [Find Property Claims](actions/find-property-claims.md) | GET | Retrieves property claims from Encircle. |
| [Get Property Claim](actions/get-property-claim.md) | GET | Retrieves a property claim from Encircle by ID. |
| [Update Property Claim](actions/update-property-claim.md) | PUT | Updates a property claim in Encircle. |

### Property Inspection

| Action | Method | Description |
| --- | --- | --- |
| [Create Property Inspection](actions/create-property-inspection.md) | POST | Creates a property inspection in Encircle. |
| [Find Property Inspections](actions/find-property-inspections.md) | GET | Retrieves property inspections from Encircle. |
| [Get Property Inspection](actions/get-property-inspection.md) | GET | Retrieves a property inspection from Encircle by ID. |
| [Update Property Inspection](actions/update-property-inspection.md) | PUT | Updates a property inspection in Encircle. |

### Room

| Action | Method | Description |
| --- | --- | --- |
| [Find Claim Rooms](actions/find-claim-rooms.md) | GET | Retrieves claim rooms from Encircle. |
| [Find Inspection Rooms](actions/find-inspection-rooms.md) | GET | Retrieves inspection rooms from Encircle. |

### Structure

| Action | Method | Description |
| --- | --- | --- |
| [Find Claim Structures](actions/find-claim-structures.md) | GET | Retrieves claim structures from Encircle. |
| [Find Inspection Structures](actions/find-inspection-structures.md) | GET | Retrieves inspection structures from Encircle. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Assign User To Claim](actions/assign-user-to-claim.md) | POST | Assigns a user to a property claim in Encircle. |
| [Find Claim Assignments](actions/find-claim-assignments.md) | GET | Retrieves claim assignments from Encircle. |
| [Find Inspection Assignments](actions/find-inspection-assignments.md) | GET | Retrieves inspection assignments from Encircle. |
| [Unassign User From Claim](actions/unassign-user-from-claim.md) | DELETE | Unassigns a user from a property claim in Encircle. |

