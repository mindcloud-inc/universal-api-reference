# Create Offer with Ghost

Creates a new offer in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/offers/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Offer](https://docs.ghost.org/admin-api/offers/creating-an-offer)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `offers[0].name` | body | `string` | yes |
| `offers[0].code` | body | `string` | yes |
| `offers[0].display_title` | body | `string` | no |
| `offers[0].display_description` | body | `string` | no |
| `offers[0].type` | body | `string` | yes |
| `offers[0].cadence` | body | `string` | yes |
| `offers[0].amount` | body | `number` | yes |
| `offers[0].duration` | body | `string` | yes |
| `offers[0].duration_in_months` | body | `number` | no |
| `offers[0].currency_restriction` | body | `boolean` | no |
| `offers[0].currency` | body | `string` | no |
| `offers[0].status` | body | `string` | no |
| `offers[0].redemption_count` | body | `number` | no |
| `offers[0].tier.id` | body | `string` | yes |
