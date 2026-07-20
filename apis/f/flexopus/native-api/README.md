# Flexopus: Native API Reference

A consolidated summary of Flexopus's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://flexopus.com/api/docs/
- **API base URL:** `{tenantBaseUrl}/api/v1`

## Authentication

### API Token

Connect Flexopus with a generated API token and your tenant base URL.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant Base URL:** `tenantBaseUrl` · required · The full Flexopus tenant base URL, for example `https://company.flexopus.com` or your custom Flexopus domain.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://flexopus.com/api/docs/#authenticating-requests)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://flexopus.com/api/docs/#endpoints-POSTapi-v1-bookings) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://flexopus.com/api/docs/#endpoints-POSTapi-v1-events) |
| [Delete Booking](actions/delete-booking.md) | `DELETE /bookings/:id` | [docs](https://flexopus.com/api/docs/#endpoints-DELETEapi-v1-bookings--id-) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/:id` | [docs](https://flexopus.com/api/docs/#endpoints-DELETEapi-v1-events--id-) |
| [Export Users](actions/export-users.md) | `GET /users/export` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users-export) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-events--id-) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users--id-) |
| [Get User by Email](actions/get-user-by-email.md) | `GET /users/by-email/:user_email` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users-by-email--user_email-) |
| [Import Users](actions/import-users.md) | `POST /users/import` | [docs](https://flexopus.com/api/docs/#endpoints-POSTapi-v1-users-import) |
| [List Bookable Bookings](actions/list-bookable-bookings.md) | `GET /bookables/:bookable_id/bookings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-bookables--bookable_id--bookings) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-bookings) |
| [List Building Bookings](actions/list-building-bookings.md) | `GET /buildings/:building_id/bookings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-buildings--building_id--bookings) |
| [List Buildings](actions/list-buildings.md) | `GET /buildings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-buildings) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-events) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-groups) |
| [List Location Bookable Occupancy](actions/list-location-bookable-occupancy.md) | `GET /locations/:location_id/bookables/occupancy` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-locations--location_id--bookables-occupancy) |
| [List Location Bookables](actions/list-location-bookables.md) | `GET /locations/:location_id/bookables` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-locations--location_id--bookables) |
| [List Location Bookings](actions/list-location-bookings.md) | `GET /locations/:location_id/bookings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-locations--location_id--bookings) |
| [List Today's Events](actions/list-todays-events.md) | `GET /events/today` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-events-today) |
| [List User Bookings](actions/list-user-bookings.md) | `GET /users/:user_id/bookings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users--user_id--bookings) |
| [List User Bookings by Email](actions/list-user-bookings-by-email.md) | `GET /users/by-email/:user_email/bookings` | [docs](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users-by-email--user_email--bookings) |
| [Update Bookable](actions/update-bookable.md) | `PATCH /bookables/:id` | [docs](https://flexopus.com/api/docs/#endpoints-PATCHapi-v1-bookables--id-) |
| [Update Booking](actions/update-booking.md) | `PUT /bookings/:id` | [docs](https://flexopus.com/api/docs/#endpoints-PUTapi-v1-bookings--id-) |
| [Update Event](actions/update-event.md) | `PUT /events/:id` | [docs](https://flexopus.com/api/docs/#endpoints-PUTapi-v1-events--id-) |
