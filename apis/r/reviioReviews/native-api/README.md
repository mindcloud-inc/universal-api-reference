# Revi.io Reviews: Native API Reference

A consolidated summary of Revi.io Reviews's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.revi7.com/
- **API base URL:** `https://api.revi.io/api/v1`

## Authentication

### API Key

Custom API key auth for Revi because the provider requires the exact shared header X-API-KEY instead of Authorization: Bearer.

### Credentials

- **API Key:** `apiKey` · required · Your Revi tenant API key.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.revi7.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Orders](actions/create-orders.md) | `POST /orders` | [docs](https://docs.revi7.com/) |
| [Create Products](actions/create-products.md) | `POST /products` | [docs](https://docs.revi7.com/) |
| [Delete Orders](actions/delete-orders.md) | `POST /orders` | [docs](https://docs.revi7.com/) |
| [Get Product Review Info](actions/get-product-review-info.md) | `GET /product_info` | [docs](https://docs.revi7.com/) |
| [Get Reviews](actions/get-reviews.md) | `GET /reviews` | [docs](https://docs.revi7.com/) |
| [Get Shop Rating Info](actions/get-shop-rating-info.md) | `GET /shop_info` | [docs](https://docs.revi7.com/) |
| [Hello World](actions/hello-world.md) | `POST /hello_world` | [docs](https://docs.revi7.com/#quickstart) |
| [Link Full Products to Orders](actions/link-full-products-to-orders.md) | `POST /orders_products` | [docs](https://docs.revi7.com/) |
| [Link Products to Orders](actions/link-products-to-orders.md) | `POST /orders_products` | [docs](https://docs.revi7.com/) |
| [Update Order Statuses](actions/update-order-statuses.md) | `POST /orders_status` | [docs](https://docs.revi7.com/) |
