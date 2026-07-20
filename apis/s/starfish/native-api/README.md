# Starfish: Native API Reference

A consolidated summary of Starfish's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://developer.camping.care/docs/api/
- **API base URL:** `https://api.camping.care/v21`

## Authentication

### API Key

Connect with a Camping.care private API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.camping.care/docs/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 15; accepted range 1–30). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Accommodation](actions/create-accommodation.md) | `POST /accommodations` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Create Place](actions/create-place.md) | `POST /accommodations/:accommodation_id/places` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Create Reservation](actions/create-reservation.md) | `POST /reservations` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Delete Accommodation](actions/delete-accommodation.md) | `DELETE /accommodations/:accommodation_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE /invoices/:invoice_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Get Accommodation](actions/get-accommodation.md) | `GET /accommodations/:accommodation_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developer.camping.care/docs/api/authentication/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Get Place](actions/get-place.md) | `GET /accommodations/:accommodation_id/places/:place_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Get Reservation](actions/get-reservation.md) | `GET /reservations/:id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [List Accommodations](actions/list-accommodations.md) | `GET /accommodations` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [List Places](actions/list-places.md) | `GET /accommodations/:accommodation_id/places` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [List Reservations](actions/list-reservations.md) | `GET /reservations` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Update Accommodation](actions/update-accommodation.md) | `PUT /accommodations/:accommodation_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoice_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
| [Update Place](actions/update-place.md) | `PUT /accommodations/:accommodation_id/places/:place_id` | [docs](https://documenter.getpostman.com/view/9467805/VUjQkj1d) |
