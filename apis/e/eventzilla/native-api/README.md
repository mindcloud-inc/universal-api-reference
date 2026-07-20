# Eventzilla: Native API Reference

A consolidated summary of Eventzilla's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://developer.eventzilla.net/docs/
- **API base URL:** `https://www.eventzillaapi.net/api/v2`

## Authentication

### API Key

Authenticate with your Eventzilla API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.eventzilla.net/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Event Order](actions/cancel-event-order.md) | `POST /events/order/cancel` | [docs](https://developer.eventzilla.net/docs/#ev_orderCAN) |
| [Confirm Checkout](actions/confirm-checkout.md) | `POST /checkout/confirm` | [docs](https://developer.eventzilla.net/docs/#confirm) |
| [Confirm Event Order](actions/confirm-event-order.md) | `POST /events/order/confirm` | [docs](https://developer.eventzilla.net/docs/#ev_orderCNF) |
| [Create Checkout](actions/create-checkout.md) | `POST /checkout/create` | [docs](https://developer.eventzilla.net/docs/#create) |
| [Fill Checkout Order](actions/fill-checkout-order.md) | `POST /checkout/fillorder` | [docs](https://developer.eventzilla.net/docs/#fill) |
| [Get Attendee](actions/get-attendee.md) | `GET /attendees/:attendeeid` | [docs](https://developer.eventzilla.net/docs/#attendees) |
| [Get Event](actions/get-event.md) | `GET /events/:eventid` | [docs](https://developer.eventzilla.net/docs/#events) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:lookup` | [docs](https://developer.eventzilla.net/docs/#transactions) |
| [Get User](actions/get-user.md) | `GET /users/:userid` | [docs](https://developer.eventzilla.net/docs/#users) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developer.eventzilla.net/docs/) |
| [List Event Attendees](actions/list-event-attendees.md) | `GET /events/:eventid/attendees` | [docs](https://developer.eventzilla.net/docs/#ev_attendee) |
| [List Event Tickets](actions/list-event-tickets.md) | `GET /events/:eventid/tickets` | [docs](https://developer.eventzilla.net/docs/#ev_tickets) |
| [List Event Transactions](actions/list-event-transactions.md) | `GET /events/:eventid/transactions` | [docs](https://developer.eventzilla.net/docs/#ev_transactions) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developer.eventzilla.net/docs/#events) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.eventzilla.net/docs/#users) |
| [Prepare Checkout](actions/prepare-checkout.md) | `GET /checkout/prepare/:eventid/:dateid` | [docs](https://developer.eventzilla.net/docs/#prepare) |
| [Toggle Event Sales](actions/toggle-event-sales.md) | `POST /events/togglesales` | [docs](https://developer.eventzilla.net/docs/#ev_toggle) |
| [Update Attendee Check-In](actions/update-attendee-check-in.md) | `POST /attendees/checkin` | [docs](https://developer.eventzilla.net/docs/#att_checkin) |
