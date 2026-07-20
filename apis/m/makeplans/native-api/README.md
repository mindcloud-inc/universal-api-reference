# Makeplans: Native API Reference

A consolidated summary of Makeplans's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.makeplans.com/
- **API base URL:** `https://{accountDomain}/api/v1`

## Authentication

### API Key

Authenticate to the Makeplans private API with an account API key sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required
- **Account domain:** `accountDomain` · required · Enter only the domain for the Makeplans account, such as youraccount.makeplans.com or youraccount.test.makeplans.net.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.makeplans.com/guide/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Makeplans` |

Responses from this API use JSON. The total page count is read from `headers.total-pages`. The current page number is read from `headers.current-page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | `PUT /bookings/:bookingId/cancel` | [docs](https://developer.makeplans.com/endpoints/bookings/) |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://developer.makeplans.com/endpoints/bookings/) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://developer.makeplans.com/endpoints/events/) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://developer.makeplans.com/endpoints/people/) |
| [Create Resource](actions/create-resource.md) | `POST /resources` | [docs](https://developer.makeplans.com/endpoints/resources/) |
| [Create Service](actions/create-service.md) | `POST /services` | [docs](https://developer.makeplans.com/endpoints/services/) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:bookingId` | [docs](https://developer.makeplans.com/endpoints/bookings/) |
| [Get Event](actions/get-event.md) | `GET /events/:eventId` | [docs](https://developer.makeplans.com/endpoints/events/) |
| [Get Person](actions/get-person.md) | `GET /people/:personId` | [docs](https://developer.makeplans.com/endpoints/people/) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:resourceId` | [docs](https://developer.makeplans.com/endpoints/resources/) |
| [Get Service](actions/get-service.md) | `GET /services/:serviceId` | [docs](https://developer.makeplans.com/endpoints/services/) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://developer.makeplans.com/endpoints/bookings/) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developer.makeplans.com/endpoints/categories/) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developer.makeplans.com/endpoints/events/) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developer.makeplans.com/endpoints/orders/) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://developer.makeplans.com/endpoints/people/) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://developer.makeplans.com/endpoints/resources/) |
| [List Service Slots](actions/list-service-slots.md) | `GET /services/:serviceId/slots` | [docs](https://developer.makeplans.com/endpoints/slots/) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://developer.makeplans.com/endpoints/services/) |
| [Update Booking](actions/update-booking.md) | `PUT /bookings/:bookingId` | [docs](https://developer.makeplans.com/endpoints/bookings/) |
| [Update Event](actions/update-event.md) | `PUT /events/:eventId` | [docs](https://developer.makeplans.com/endpoints/events/) |
| [Update Person](actions/update-person.md) | `PUT /people/:personId` | [docs](https://developer.makeplans.com/endpoints/people/) |
| [Update Resource](actions/update-resource.md) | `PUT /resources/:resourceId` | [docs](https://developer.makeplans.com/endpoints/resources/) |
| [Update Service](actions/update-service.md) | `PUT /services/:serviceId` | [docs](https://developer.makeplans.com/endpoints/services/) |
