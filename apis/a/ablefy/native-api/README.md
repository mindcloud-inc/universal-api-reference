# Ablefy: Native API Reference

A consolidated summary of Ablefy's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.myablefy.com/api/swagger_doc/
- **OpenAPI specification:** https://api.myablefy.com/api/swagger_doc/
- **API base URL:** `https://api.myablefy.com`

## Authentication

### API Key

API key authentication for the Ablefy API

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.ablefy.io/seller/articles/en_US/Knowledge/ablefy-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | `POST /api/orders/:token/cancel` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Create Funnel](actions/create-funnel.md) | `POST /api/funnels` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Create Order](actions/create-order.md) | `POST /api/orders` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Create Product](actions/create-product.md) | `POST /api/products` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /api/webhook_endpoints` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Delete Funnel](actions/delete-funnel.md) | `DELETE /api/funnels/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Delete Pricing Plan](actions/delete-pricing-plan.md) | `DELETE /api/pricing_plans/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /api/webhook_endpoints/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Account](actions/get-account.md) | `GET /api/me` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Funnel](actions/get-funnel.md) | `GET /api/funnels/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Order](actions/get-order.md) | `GET /api/orders/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Payment](actions/get-payment.md) | `GET /api/payments/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Pricing Plan](actions/get-pricing-plan.md) | `GET /api/pricing_plans/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Product](actions/get-product.md) | `GET /api/products/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | `GET /api/webhook_endpoints/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [List Funnels](actions/list-funnels.md) | `GET /api/funnels` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [List Invoices](actions/list-invoices.md) | `GET /api/invoices` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [List Pricing Plans](actions/list-pricing-plans.md) | `GET /api/pricing_plans` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [List Products](actions/list-products.md) | `GET /api/products` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /api/webhook_endpoints` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Refund Payment](actions/refund-payment.md) | `POST /api/payments/:id/refund` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Update Funnel](actions/update-funnel.md) | `PUT /api/funnels/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Update Product](actions/update-product.md) | `PUT /api/products/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PUT /api/webhook_endpoints/:id` | [docs](https://api.myablefy.com/api/swagger_doc/) |
