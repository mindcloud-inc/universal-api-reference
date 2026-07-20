# Flexport: Native API Reference

A consolidated summary of Flexport's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.flexport.com/
- **API base URL:** `https://api.flexport.com`

## Authentication

### OAuth2 Client Credentials

Use Flexport API Credentials (client ID and client secret) to obtain a bearer token for Flexport public API requests.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.flexport.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.flexport.com/tutorials/using-api-credentials/)

### API Key

Use a Flexport API Key bearer token for runtime verification and API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.flexport.com/tutorials/using-api-credentials/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Product#operation/products_create) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Booking#operation/bookings_index) |
| [List Containers](actions/list-containers.md) | `GET /ocean/shipment_containers` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Container#operation/container_list) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Product#operation/products_index) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Shipment#operation/shipment_index) |
| [Retrieve Booking](actions/retrieve-booking.md) | `GET /bookings/:id` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Booking#operation/bookings_show) |
| [Retrieve Container](actions/retrieve-container.md) | `GET /ocean/shipment_containers/:id` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Container#operation/container_show) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /products/:id` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Product#operation/products_show) |
| [Retrieve Shipment](actions/retrieve-shipment.md) | `GET /shipments/:id` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Shipment#operation/shipment_show) |
| [Update Product](actions/update-product.md) | `PATCH /products/:id` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Product#operation/products_update) |
| [Update Shipment](actions/update-shipment.md) | `PATCH /shipments/:id` | [docs](https://apidocs.flexport.com/2023-07-01/tag/Shipment#operation/shipment_update) |
