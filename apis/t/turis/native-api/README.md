# Turis: Native API Reference

A consolidated summary of Turis's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/16452985/TzkyP1Er
- **API base URL:** `https://{tenant}.turis.app`

## Authentication

### OAuth 2.0 (Client Credentials)

Machine-to-machine OAuth2 for Turis using tenant, client ID, and client secret. This flow does not open a browser authorization page.

### Credentials

- **Tenant:** `tenant` · required · Your Turis account name without .turis.app, for example test from test.turis.app.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://{{credentials.tenant}}.turis.app/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://documenter.getpostman.com/view/16452985/TzkyP1Er)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Products to Order](actions/add-products-to-order.md) | `POST /api/public/v1/orders/:orderId/products/add` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Buyer](actions/create-buyer.md) | `POST /api/public/v1/buyers` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Category](actions/create-category.md) | `POST /api/public/v1/categories` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Company](actions/create-company.md) | `POST /api/public/v1/companies` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Delivery](actions/create-delivery.md) | `POST /api/public/v1/deliveries` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Order](actions/create-order.md) | `POST /api/public/v1/orders` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Product](actions/create-product.md) | `POST /api/public/v1/products` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Create Tags](actions/create-tags.md) | `POST /api/public/v1/tags` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Get Buyer](actions/get-buyer.md) | `GET /api/public/v1/buyers/:buyerId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Get Company](actions/get-company.md) | `GET /api/public/v1/companies/:companyId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Get Order](actions/get-order.md) | `GET /api/public/v1/orders/:orderId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Get Product](actions/get-product.md) | `GET /api/public/v1/products/:productId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Buyers](actions/list-buyers.md) | `GET /api/public/v1/buyers` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Categories](actions/list-categories.md) | `GET /api/public/v1/categories` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Companies](actions/list-companies.md) | `GET /api/public/v1/companies` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Currencies](actions/list-currencies.md) | `GET /api/public/v1/currencies` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Deliveries](actions/list-deliveries.md) | `GET /api/public/v1/deliveries` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /api/public/v1/order-statuses` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Orders](actions/list-orders.md) | `GET /api/public/v1/orders` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Orders by Status](actions/list-orders-by-status.md) | `GET /api/public/v1/orders/status/:statusId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Orders Updated Between Dates](actions/list-orders-updated-between-dates.md) | `GET /api/public/v1/orders/updated/:from/:to` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Products](actions/list-products.md) | `GET /api/public/v1/products` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [List Tags](actions/list-tags.md) | `GET /api/public/v1/tags` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Buyer](actions/update-buyer.md) | `PUT /api/public/v1/buyers/:buyerId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Company](actions/update-company.md) | `PUT /api/public/v1/companies/:companyId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Delivery](actions/update-delivery.md) | `PATCH /api/public/v1/deliveries/:delivery` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Order](actions/update-order.md) | `PUT /api/public/v1/orders/:orderId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Order Items](actions/update-order-items.md) | `PUT /api/public/v1/orders/:orderId/items` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Order Tags](actions/update-order-tags.md) | `PATCH /api/public/v1/orders/:orderId/tags` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Product](actions/update-product.md) | `PATCH /api/public/v1/products/:productId` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
| [Update Product Inventory](actions/update-product-inventory.md) | `PATCH /api/public/v1/products/bulk/inventory-update` | [docs](https://documenter.getpostman.com/view/16452985/TzkyP1Er) |
