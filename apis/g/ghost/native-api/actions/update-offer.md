# Update Offer with Ghost

Updates an existing offer in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/offers/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Update Offer](https://docs.ghost.org/admin-api/offers/updating-an-offer)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `offers[0].name` | body | `string` | no |
| `offers[0].code` | body | `string` | no |
| `offers[0].display_title` | body | `string` | no |
| `offers[0].display_description` | body | `string` | no |
