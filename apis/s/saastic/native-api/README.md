# Saastic: Native API Reference

A consolidated summary of Saastic's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.moregoodreviews.com/platform/api-reference
- **API base URL:** `https://api.moregoodreviews.com`

## Authentication

### API Key

Use the project API key as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.moregoodreviews.com/platform/api-reference)

## API conventions

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `pagination.last_page`. The current page number is read from `pagination.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer Charge](actions/create-customer-charge.md) | `POST /beacon/charges` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [Create Location](actions/create-location.md) | `POST /beacon/locations` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [Create or Update Customer](actions/create-or-update-customer.md) | `POST /beacon/customers` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [Create Review Request](actions/create-review-request.md) | `POST /beacon/asks` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [List Customer Messages](actions/list-customer-messages.md) | `GET /beacon/customers/:id/messages` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [List Customer Reviews](actions/list-customer-reviews.md) | `GET /beacon/customers/:id/reviews` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [List Customers](actions/list-customers.md) | `GET /beacon/customers` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [List Reviews](actions/list-reviews.md) | `GET /beacon/reviews` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
| [Update Location](actions/update-location.md) | `PUT /beacon/locations/:id` | [docs](https://docs.moregoodreviews.com/platform/api-reference) |
