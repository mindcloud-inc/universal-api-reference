# TicketSource: Native API Reference

A consolidated summary of TicketSource's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://reference.ticketsource.io/
- **OpenAPI specification:** https://raw.githubusercontent.com/ticketsource/openapi-spec/main/reference/TicketSource-API.json
- **API base URL:** `https://api.ticketsource.io`

## Authentication

### API Key

Use your TicketSource API key to connect.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ticketsource.io/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `after`, `before`, `between`, `on`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://www.ticketsource.io/working-with-customers) |
| [Create Customer Note](actions/create-customer-note.md) | `POST /customers/{CustomerId}/notes` | [docs](https://www.ticketsource.io/working-with-customers) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/{CustomerId}` | [docs](https://www.ticketsource.io/working-with-customers) |
| [Delete Customer Note](actions/delete-customer-note.md) | `DELETE /customers/{CustomerId}/notes/{CustomerNoteId}` | [docs](https://www.ticketsource.io/working-with-customers) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/{BookingId}` | [docs](https://www.ticketsource.io/working-with-bookings) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{CustomerId}` | [docs](https://www.ticketsource.io/working-with-customers) |
| [Get Customer Note](actions/get-customer-note.md) | `GET /customers/{CustomerId}/notes/{CustomerNoteId}` | [docs](https://www.ticketsource.io/working-with-customers) |
| [Get Date](actions/get-date.md) | `GET /dates/{DateId}` | [docs](https://www.ticketsource.io/working-with-events) |
| [Get Event](actions/get-event.md) | `GET /events/{EventId}` | [docs](https://www.ticketsource.io/working-with-events) |
| [Get Seat](actions/get-seat.md) | `GET /seats/{SeatId}` | [docs](https://www.ticketsource.io/working-with-bookings) |
| [Get Venue](actions/get-venue.md) | `GET /venues/{VenueId}` | [docs](https://www.ticketsource.io/working-with-events) |
| [List Booking Seats](actions/list-booking-seats.md) | `GET /bookings/{BookingId}/seats` | [docs](https://www.ticketsource.io/working-with-bookings) |
| [List Customer Bookings](actions/list-customer-bookings.md) | `GET /customers/{CustomerId}/bookings` | [docs](https://www.ticketsource.io/working-with-bookings) |
| [List Customer Notes](actions/list-customer-notes.md) | `GET /customers/{CustomerId}/notes` | [docs](https://www.ticketsource.io/working-with-customers) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.ticketsource.io/working-with-customers) |
| [List Date Bookings](actions/list-date-bookings.md) | `GET /dates/{DateId}/bookings` | [docs](https://www.ticketsource.io/working-with-bookings) |
| [List Event Dates](actions/list-event-dates.md) | `GET /events/{EventId}/dates` | [docs](https://www.ticketsource.io/working-with-events) |
| [List Event Venues](actions/list-event-venues.md) | `GET /events/{EventId}/venues` | [docs](https://www.ticketsource.io/working-with-events) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://www.ticketsource.io/working-with-events) |
| [List Venue Dates](actions/list-venue-dates.md) | `GET /venues/{VenueId}/dates` | [docs](https://www.ticketsource.io/working-with-events) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/{CustomerId}` | [docs](https://www.ticketsource.io/working-with-customers) |
