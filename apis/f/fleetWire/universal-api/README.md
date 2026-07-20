# <img src="https://images.mindcloud.co/apps/icons/fleet-wire_1775134823301.png" alt="FleetWire logo" width="28" height="28"> FleetWire: Universal API

FleetWire gives rental operators API access to bookings, listings, pricing, extras, and tenant activity feeds using bearer API tokens.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fleetWire/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fleetwire.io
- **Vendor API docs:** https://documenter.getpostman.com/view/263138/Tz5p6dWS

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bookings](actions/list-bookings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Abandoned Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Abandoned Bookings](actions/list-abandoned-bookings.md) | GET | Retrieves abandoned bookings from FleetWire. |

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Listing Availability](actions/get-listing-availability.md) | GET | Retrieves listing availability from FleetWire. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from FleetWire. |
| [Update Booking Status](actions/update-booking-status.md) | PUT | Updates an existing booking status in FleetWire. |

### Booking Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Zapier Booking](actions/get-zapier-booking.md) | GET | Retrieves a Zapier booking from FleetWire. |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in FleetWire. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from FleetWire. |

### Extra

| Action | Method | Description |
| --- | --- | --- |
| [List Extras](actions/list-extras.md) | GET | Retrieves extras from FleetWire. |

### Listing

| Action | Method | Description |
| --- | --- | --- |
| [Get Listing](actions/get-listing.md) | GET | Retrieves a listing from FleetWire. |
| [List Listings](actions/list-listings.md) | GET | Retrieves listings from FleetWire. |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Listing Daily Pricing](actions/get-listing-daily-pricing.md) | GET | Retrieves listing daily pricing from FleetWire. |

