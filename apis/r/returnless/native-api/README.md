# Returnless: Native API Reference

A consolidated summary of Returnless's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.returnless.com/docs/api-rest-reference/64548cf9032b4
- **API base URL:** `https://api-v2.returnless.com`

## Authentication

### API Key

Bearer API key authentication for the Returnless REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.returnless.com/docs/api-rest-reference/vlfd96x8lqzgf)

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Return Order Item](actions/add-return-order-item.md) | `POST /2025-01/return-orders/{returnOrder}/items` | [docs](https://docs.returnless.com/docs/api-rest-reference/7faacd6288c63) |
| [Add Return Order Note](actions/add-return-order-note.md) | `POST /2025-01/return-orders/{returnOrder}/notes` | [docs](https://docs.returnless.com/docs/api-rest-reference/1aa005cc39ee0) |
| [Add Return Order Shipment](actions/add-return-order-shipment.md) | `POST /2025-01/return-orders/{returnOrder}/shipments` | [docs](https://docs.returnless.com/docs/api-rest-reference/455a6fbc1d4eb) |
| [Approve Return Order](actions/approve-return-order.md) | `POST /2025-01/return-orders/{returnOrder}/approve` | [docs](https://docs.returnless.com/docs/api-rest-reference/c3a41f4317680) |
| [Attach Return Order Tags](actions/attach-return-order-tags.md) | `POST /2025-01/return-orders/{returnOrder}/tags` | [docs](https://docs.returnless.com/docs/api-rest-reference/1303b1f885b0a) |
| [Create Return Order](actions/create-return-order.md) | `POST /2025-01/return-orders` | [docs](https://docs.returnless.com/docs/api-rest-reference/1fce50b07484b) |
| [Detach Return Order Tags](actions/detach-return-order-tags.md) | `DELETE /2025-01/return-orders/{returnOrder}/tags` | [docs](https://docs.returnless.com/docs/api-rest-reference/13505cb7e1fbe) |
| [Get Current Account](actions/get-current-account.md) | `GET /2025-01/account` | [docs](https://docs.returnless.com/docs/api-rest-reference/0f01a727c340d) |
| [Get Customer](actions/get-customer.md) | `GET /2025-01/customers/{customer}` | [docs](https://docs.returnless.com/docs/api-rest-reference/9c710943d5036) |
| [Get Product](actions/get-product.md) | `GET /2025-01/products/{product}` | [docs](https://docs.returnless.com/docs/api-rest-reference/94c4ade905c79) |
| [Get Return Order](actions/get-return-order.md) | `GET /2025-01/return-orders/{returnOrder}` | [docs](https://docs.returnless.com/docs/api-rest-reference/f670282943eae) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /2025-01/sales-orders/{salesOrder}` | [docs](https://docs.returnless.com/docs/api-rest-reference/4a6a8fe812c44) |
| [Get Shipment](actions/get-shipment.md) | `GET /2025-01/shipments/{shipment}` | [docs](https://docs.returnless.com/docs/api-rest-reference/8add0ab769032) |
| [List Customer Addresses](actions/list-customer-addresses.md) | `GET /2025-01/customers/{customer}/addresses` | [docs](https://docs.returnless.com/docs/api-rest-reference/433697148bc5c) |
| [List Customer Groups](actions/list-customer-groups.md) | `GET /2025-01/customers/{customer}/customer-groups` | [docs](https://docs.returnless.com/docs/api-rest-reference/f4fa0f9f1a95e) |
| [List Customer Return Orders](actions/list-customer-return-orders.md) | `GET /2025-01/customers/{customer}/return-orders` | [docs](https://docs.returnless.com/docs/api-rest-reference/ed737183af993) |
| [List Customers](actions/list-customers.md) | `GET /2025-01/customers` | [docs](https://docs.returnless.com/docs/api-rest-reference/0436afe351619) |
| [List Products](actions/list-products.md) | `GET /2025-01/products` | [docs](https://docs.returnless.com/docs/api-rest-reference/d064e56094cd6) |
| [List Return Order Items](actions/list-return-order-items.md) | `GET /2025-01/return-orders/{returnOrder}/items` | [docs](https://docs.returnless.com/docs/api-rest-reference/b6c4c8fe65c93) |
| [List Return Order Metadata](actions/list-return-order-metadata.md) | `GET /2025-01/return-orders/{returnOrder}/meta-data` | [docs](https://docs.returnless.com/docs/api-rest-reference/d88519cafe174) |
| [List Return Order Notes](actions/list-return-order-notes.md) | `GET /2025-01/return-orders/{returnOrder}/notes` | [docs](https://docs.returnless.com/docs/api-rest-reference/71b1c8cd85421) |
| [List Return Order Shipments](actions/list-return-order-shipments.md) | `GET /2025-01/return-orders/{returnOrder}/shipments` | [docs](https://docs.returnless.com/docs/api-rest-reference/1e0748fdd876f) |
| [List Return Order Tags](actions/list-return-order-tags.md) | `GET /2025-01/return-orders/{returnOrder}/tags` | [docs](https://docs.returnless.com/docs/api-rest-reference/d4d37e2232a35) |
| [List Return Orders](actions/list-return-orders.md) | `GET /2025-01/return-orders` | [docs](https://docs.returnless.com/docs/api-rest-reference/0640e3c064cdc) |
| [List Sales Order Items](actions/list-sales-order-items.md) | `GET /2025-01/sales-orders/{salesOrder}/items` | [docs](https://docs.returnless.com/docs/api-rest-reference/6b3c26dad0434) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /2025-01/sales-orders` | [docs](https://docs.returnless.com/docs/api-rest-reference/ce6a0e3d66378) |
| [List Shipments](actions/list-shipments.md) | `GET /2025-01/shipments` | [docs](https://docs.returnless.com/docs/api-rest-reference/7daf3fa2c9bf9) |
| [Reject Return Order](actions/reject-return-order.md) | `POST /2025-01/return-orders/{returnOrder}/reject` | [docs](https://docs.returnless.com/docs/api-rest-reference/e5d201fe70527) |
| [Update Return Order Metadata](actions/update-return-order-metadata.md) | `PUT /2025-01/return-orders/{returnOrder}/meta-data` | [docs](https://docs.returnless.com/docs/api-rest-reference/90f9683baeca5) |
| [Update Return Order Status](actions/update-return-order-status.md) | `PATCH /2025-01/return-orders/{returnOrder}/status` | [docs](https://docs.returnless.com/docs/api-rest-reference/1d07e272437a4) |
