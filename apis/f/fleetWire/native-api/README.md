# FleetWire: Native API Reference

A consolidated summary of FleetWire's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/263138/Tz5p6dWS
- **API base URL:** `https://api.fleetwire.io`

## Authentication

### API Key

Use a FleetWire API token from Company Settings > Security > API Tokens. Requests authenticate with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.fleetwire.io/en/article/introduction-to-the-fleetwire-api-izq6u/)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | `POST /api/v1/checkout` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [Get Company](actions/get-company.md) | `GET /api/v2/company/:company` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [Get Listing](actions/get-listing.md) | `GET /api/v2/listings/:l_id` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [Get Listing Availability](actions/get-listing-availability.md) | `GET /api/v2/listings/availability` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [Get Listing Daily Pricing](actions/get-listing-daily-pricing.md) | `GET /api/v2/listings/:l_id/daily_pricing` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [Get Zapier Booking](actions/get-zapier-booking.md) | `GET /api/v2/zapier/bookings/:b_id` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [List Abandoned Bookings](actions/list-abandoned-bookings.md) | `GET /api/v2/zapier/abandoned-bookings` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [List Bookings](actions/list-bookings.md) | `GET /api/v2/bookings` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [List Extras](actions/list-extras.md) | `GET /api/v2/extras-v2` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [List Listings](actions/list-listings.md) | `GET /api/v2/listings` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
| [Update Booking Status](actions/update-booking-status.md) | `PUT /api/v2/bookings/:booking_id/status` | [docs](https://documenter.getpostman.com/view/263138/Tz5p6dWS) |
