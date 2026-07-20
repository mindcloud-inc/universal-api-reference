# Update Venue with Eventbrite

Updates an existing venue in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/venues/:venueId/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Update Venue](https://www.eventbrite.com/platform/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `venue.address.address_1` | body | `string` | yes | Street address line 1. |
| `venue.address.city` | body | `string` | yes | City. |
| `venue.address.country` | body | `string` | yes | Two-letter country code (e.g. US). |
| `venue.address.postal_code` | body | `string` | yes | Postal code. |
| `venue.address.region` | body | `string` | yes | State/region code. |
| `venue.name` | body | `string` | yes | Venue display name. |
| `venueId` | path | `string` | yes | Venue identifier. |
