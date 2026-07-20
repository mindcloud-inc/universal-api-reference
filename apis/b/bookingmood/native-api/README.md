# Bookingmood: Native API Reference

A consolidated summary of Bookingmood's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.bookingmood.com/en-US/api-reference
- **API base URL:** `https://api.bookingmood.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.bookingmood.com/en-US/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (maximum 1000). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string. Supported operators: `eq`, `like`.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Book](actions/book.md) | `POST /book` | [docs](https://www.bookingmood.com/en-US/api-reference/book) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.bookingmood.com/en-US/api-reference/contacts) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://www.bookingmood.com/en-US/api-reference/invoices) |
| [Create Payment](actions/create-payment.md) | `POST /payments` | [docs](https://www.bookingmood.com/en-US/api-reference/payments) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://www.bookingmood.com/en-US/api-reference/products) |
| [Delete Bookings](actions/delete-bookings.md) | `DELETE /bookings` | [docs](https://www.bookingmood.com/en-US/api-reference/bookings) |
| [Delete Calendar Events](actions/delete-calendar-events.md) | `DELETE /calendar_events` | [docs](https://www.bookingmood.com/en-US/api-reference/calendar_events) |
| [Delete Contacts](actions/delete-contacts.md) | `DELETE /contacts` | [docs](https://www.bookingmood.com/en-US/api-reference/contacts) |
| [Delete Products](actions/delete-products.md) | `DELETE /products` | [docs](https://www.bookingmood.com/en-US/api-reference/products) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://www.bookingmood.com/en-US/api-reference/bookings) |
| [List Calendar Events](actions/list-calendar-events.md) | `GET /calendar_events` | [docs](https://www.bookingmood.com/en-US/api-reference/calendar_events) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.bookingmood.com/en-US/api-reference/contacts) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://www.bookingmood.com/en-US/api-reference/invoices) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://www.bookingmood.com/en-US/api-reference/messages) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://www.bookingmood.com/en-US/api-reference/payments) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://www.bookingmood.com/en-US/api-reference/products) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://www.bookingmood.com/en-US/api-reference/sites) |
| [Query Availability](actions/query-availability.md) | `GET /availability` | [docs](https://www.bookingmood.com/en-US/api-reference/availability) |
| [Search Availability](actions/search-availability.md) | `POST /search` | [docs](https://www.bookingmood.com/en-US/api-reference/search) |
| [Update Bookings](actions/update-bookings.md) | `PATCH /bookings` | [docs](https://www.bookingmood.com/en-US/api-reference/bookings) |
| [Update Calendar Events](actions/update-calendar-events.md) | `PATCH /calendar_events` | [docs](https://www.bookingmood.com/en-US/api-reference/calendar_events) |
| [Update Contacts](actions/update-contacts.md) | `PATCH /contacts` | [docs](https://www.bookingmood.com/en-US/api-reference/contacts) |
| [Update Payments](actions/update-payments.md) | `PATCH /payments` | [docs](https://www.bookingmood.com/en-US/api-reference/payments) |
| [Update Products](actions/update-products.md) | `PATCH /products` | [docs](https://www.bookingmood.com/en-US/api-reference/products) |
