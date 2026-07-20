# Ticket Tailor: Native API Reference

A consolidated summary of Ticket Tailor's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.tickettailor.com/docs/intro/
- **API base URL:** `https://api.tickettailor.com`

## Authentication

### HTTP Basic Auth

Connect Ticket Tailor with HTTP Basic auth using your API key as the username.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://help.tickettailor.com/en/articles/4593218-how-do-i-connect-to-the-ticket-tailor-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 100). Use `starting_after` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Checkout Form Element](actions/get-checkout-form-element.md) | `GET /v1/checkout_forms/:checkout_form_id/elements/:checkout_form_element_id` | [docs](https://developers.tickettailor.com/docs/api/get-checkout-form-element-by-id/) |
| [Get Discount](actions/get-discount.md) | `GET /v1/discounts/:discount_id` | [docs](https://developers.tickettailor.com/docs/api/get-discount-by-id/) |
| [Get Event](actions/get-event.md) | `GET /v1/events/:event_id` | [docs](https://developers.tickettailor.com/docs/api/get-event-by-id/) |
| [Get Event Occurrence](actions/get-event-occurrence.md) | `GET /v1/event_series/:event_series_id/events/:event_occurrence_id` | [docs](https://developers.tickettailor.com/docs/api/get-event-occurrence-by-id/) |
| [Get Event Series](actions/get-event-series.md) | `GET /v1/event_series/:event_series_id` | [docs](https://developers.tickettailor.com/docs/api/get-event-series-by-id/) |
| [Get Hold](actions/get-hold.md) | `GET /v1/holds/:hold_id` | [docs](https://developers.tickettailor.com/docs/api/get-hold-by-id/) |
| [Get Issued Ticket](actions/get-issued-ticket.md) | `GET /v1/issued_tickets/:issued_ticket_id` | [docs](https://developers.tickettailor.com/docs/api/get-issued-ticket-by-id/) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/:order_id` | [docs](https://developers.tickettailor.com/docs/api/get-order-by-id/) |
| [Get Overview](actions/get-overview.md) | `GET /v1/overview` | [docs](https://developers.tickettailor.com/docs/api/get-overview/) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:product_id` | [docs](https://developers.tickettailor.com/docs/api/get-product-by-id/) |
| [Get Store](actions/get-store.md) | `GET /v1/stores/:store_id` | [docs](https://developers.tickettailor.com/docs/api/get-store-by-id/) |
| [List Check Ins](actions/list-check-ins.md) | `GET /v1/check_ins` | [docs](https://developers.tickettailor.com/docs/api/get-check-in-list/) |
| [List Checkout Form Elements](actions/list-checkout-form-elements.md) | `GET /v1/checkout_forms/:checkout_form_id/elements` | [docs](https://developers.tickettailor.com/docs/api/get-checkout-form-elements-by-custom-form-id/) |
| [List Checkout Forms](actions/list-checkout-forms.md) | `GET /v1/checkout_forms` | [docs](https://developers.tickettailor.com/docs/api/get-checkout-form-list/) |
| [List Discounts](actions/list-discounts.md) | `GET /v1/discounts` | [docs](https://developers.tickettailor.com/docs/api/get-discount-list/) |
| [List Event Occurrences](actions/list-event-occurrences.md) | `GET /v1/event_series/:event_series_id/events` | [docs](https://developers.tickettailor.com/docs/api/get-all-event-occurrences/) |
| [List Event Series](actions/list-event-series.md) | `GET /v1/event_series` | [docs](https://developers.tickettailor.com/docs/api/get-all-event-series/) |
| [List Events](actions/list-events.md) | `GET /v1/events` | [docs](https://developers.tickettailor.com/docs/api/get-all-events/) |
| [List Holds](actions/list-holds.md) | `GET /v1/holds` | [docs](https://developers.tickettailor.com/docs/api/get-hold-list/) |
| [List Issued Tickets](actions/list-issued-tickets.md) | `GET /v1/issued_tickets` | [docs](https://developers.tickettailor.com/docs/api/get-all-issued-tickets/) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://developers.tickettailor.com/docs/api/get-all-orders/) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://developers.tickettailor.com/docs/api/get-product-list/) |
| [List Stores](actions/list-stores.md) | `GET /v1/stores` | [docs](https://developers.tickettailor.com/docs/api/get-store-list/) |
| [Ping](actions/ping.md) | `GET /v1/ping` | [docs](https://developers.tickettailor.com/docs/api/ping/) |
