# Create Organization Venue with Eventbrite

Creates a new organization venue in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationId/venues/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Create Organization Venue](https://www.eventbrite.com/platform/api#/reference/venue/create/create-a-venue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization identifier. |
| `venue.address.address_1` | body | `string` | yes | Street address line 1. |
| `venue.address.city` | body | `string` | yes | City. |
| `venue.address.country` | body | `string` | yes | Two-letter country code (e.g. US). |
| `venue.address.postal_code` | body | `string` | yes | Postal code. |
| `venue.address.region` | body | `string` | yes | State/region code. |
| `venue.name` | body | `string` | yes | Venue display name. |
