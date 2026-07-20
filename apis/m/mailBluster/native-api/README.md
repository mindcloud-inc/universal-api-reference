# MailBluster: Native API Reference

A consolidated summary of MailBluster's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://app.mailbluster.com/api-doc
- **API base URL:** `https://api.mailbluster.com/api`

## Authentication

### API Key

Use a MailBluster brand API key. MailBluster accepts the raw key in the Authorization header on each API request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://app.mailbluster.com/api-doc/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://app.mailbluster.com/api-doc/leads/create) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://app.mailbluster.com/api-doc/orders/create) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://app.mailbluster.com/api-doc/products/create) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /leads/:leadHash` | [docs](https://app.mailbluster.com/api-doc/leads/delete) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/:orderId` | [docs](https://app.mailbluster.com/api-doc/orders/delete) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/:productId` | [docs](https://app.mailbluster.com/api-doc/products/delete) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadHash` | [docs](https://app.mailbluster.com/api-doc/leads/read) |
| [Get Order](actions/get-order.md) | `GET /orders/:orderId` | [docs](https://app.mailbluster.com/api-doc/orders/read) |
| [Get Product](actions/get-product.md) | `GET /products/:productId` | [docs](https://app.mailbluster.com/api-doc/products/read) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://app.mailbluster.com/api-doc/fields/read) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://app.mailbluster.com/api-doc/orders/read) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://app.mailbluster.com/api-doc/products/read) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/:leadHash` | [docs](https://app.mailbluster.com/api-doc/leads/update) |
| [Update Order](actions/update-order.md) | `PUT /orders/:orderId` | [docs](https://app.mailbluster.com/api-doc/orders/update) |
| [Update Product](actions/update-product.md) | `PUT /products/:productId` | [docs](https://app.mailbluster.com/api-doc/products/update) |
