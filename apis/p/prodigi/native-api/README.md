# Prodigi: Native API Reference

A consolidated summary of Prodigi's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.prodigi.com/print-api/docs/
- **API base URL:** `https://api.prodigi.com/v4.0`

## Authentication

### API Key

Use a Prodigi Print API key. Prodigi requires each API request to include the key in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.prodigi.com/print-api/docs/reference/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextUrl`.

## Pagination

Use `top` in the query string to set the page size (default 10; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `500`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | `POST /orders/[:prodigiOrderId]/actions/cancel` | [docs](https://www.prodigi.com/print-api/docs/reference/#cancel-an-order) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://www.prodigi.com/print-api/docs/reference/#create-order) |
| [Create Quote](actions/create-quote.md) | `POST /quotes` | [docs](https://www.prodigi.com/print-api/docs/reference/#create-quote) |
| [Get Order](actions/get-order.md) | `GET /orders/[:prodigiOrderId]` | [docs](https://www.prodigi.com/print-api/docs/reference/#get-order-by-id) |
| [Get Order Actions](actions/get-order-actions.md) | `GET /orders/[:prodigiOrderId]/actions` | [docs](https://www.prodigi.com/print-api/docs/reference/#get-actions) |
| [Get Photobook Spine Details](actions/get-photobook-spine-details.md) | `POST /products/spine` | [docs](https://www.prodigi.com/print-api/docs/reference/#get-photobook-spine-details) |
| [Get Product Details](actions/get-product-details.md) | `GET /products/[:sku]` | [docs](https://www.prodigi.com/print-api/docs/reference/#get-product-details) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://www.prodigi.com/print-api/docs/reference/#get-orders) |
| [Update Order Metadata](actions/update-order-metadata.md) | `POST /orders/[:prodigiOrderId]/actions/updateMetadata` | [docs](https://www.prodigi.com/print-api/docs/reference/#update-metadata) |
| [Update Order Recipient](actions/update-order-recipient.md) | `POST /orders/[:prodigiOrderId]/actions/updateRecipient` | [docs](https://www.prodigi.com/print-api/docs/reference/#update-recipient) |
| [Update Order Shipping Method](actions/update-order-shipping-method.md) | `POST /orders/[:prodigiOrderId]/actions/updateShippingMethod` | [docs](https://www.prodigi.com/print-api/docs/reference/#update-shipping-method) |
