# Restoplace: Native API Reference

A consolidated summary of Restoplace's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://restoplace.cc/help/API
- **API base URL:** `https://api.restoplace.cc`

## Authentication

### API Key

Use the API key generated for the Restoplace address you want to manage.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://restoplace.cc/help/API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `responseData`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Deposit](actions/calculate-deposit.md) | `POST /deposit/` | [docs](https://restoplace.cc/help/API) |
| [Create Reservation](actions/create-reservation.md) | `POST /reserves/` | [docs](https://restoplace.cc/help/API) |
| [Get Address Info](actions/get-address-info.md) | `GET /info/` | [docs](https://restoplace.cc/help/API) |
| [Get Booking Item](actions/get-booking-item.md) | `GET /items/:id` | [docs](https://restoplace.cc/help/API) |
| [Get Hall](actions/get-hall.md) | `GET /halls/:id` | [docs](https://restoplace.cc/help/API) |
| [Get Reservation](actions/get-reservation.md) | `GET /reserves/:id` | [docs](https://restoplace.cc/help/API) |
| [List Available Times](actions/list-available-times.md) | `GET /times/` | [docs](https://restoplace.cc/help/API) |
| [List Booking Items](actions/list-booking-items.md) | `GET /items` | [docs](https://restoplace.cc/help/API) |
| [List Events](actions/list-events.md) | `GET /events/` | [docs](https://restoplace.cc/help/API) |
| [List Halls](actions/list-halls.md) | `GET /halls` | [docs](https://restoplace.cc/help/API) |
| [List Item Types](actions/list-item-types.md) | `GET /itemTypes` | [docs](https://restoplace.cc/help/API) |
| [List Reservation Cancel Reasons](actions/list-reservation-cancel-reasons.md) | `GET /reserves/cancel-reasons` | [docs](https://restoplace.cc/help/API) |
| [List Reservations](actions/list-reservations.md) | `GET /reserves` | [docs](https://restoplace.cc/help/API) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets/` | [docs](https://restoplace.cc/help/API) |
| [Update Booking Item](actions/update-booking-item.md) | `PUT /items/:id` | [docs](https://restoplace.cc/help/API) |
| [Update Reservation](actions/update-reservation.md) | `PUT /reserves/:id` | [docs](https://restoplace.cc/help/API) |
| [Update Reservation Status](actions/update-reservation-status.md) | `PUT /reserves/:id/status` | [docs](https://restoplace.cc/help/API) |
