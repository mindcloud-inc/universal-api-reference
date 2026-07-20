# Sellty: Native API Reference

A consolidated summary of Sellty's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://my.sellty.ru/seller/api/documentation/
- **OpenAPI specification:** https://my.sellty.ru/seller/docs/api-docs.json
- **API base URL:** `https://my.sellty.ru`

## Authentication

### Sellty token authentication

Exchange a Sellty API login and password for the Authorization token required by Sellty v1 API endpoints.

### Credentials

- **Login:** `login` · required · Sellty API login used by POST /seller/api/v-1-0/auth.
- **Password:** `password` · required · Sellty API password used by POST /seller/api/v-1-0/auth.

Send these headers with each API request:

```http
Authorization: <custom.authorization>
```

[Official authentication documentation](https://my.sellty.ru/seller/docs/api-docs.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `limit` in the request body to set the page size (default 20; accepted range 1–100). Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /seller/api/v-1-0/auth` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [Create Product](actions/create-product.md) | `POST /seller/api/v-1-0/add-product` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [Delete Product](actions/delete-product.md) | `POST /seller/api/v-1-0/delete-product` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [Get Order](actions/get-order.md) | `POST /seller/api/v-1-0/get-order/{order}` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [List Categories](actions/list-categories.md) | `POST /seller/api/v-1-0/get-categories` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [List Groups](actions/list-groups.md) | `POST /seller/api/v-1-0/get-groups` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [List Orders](actions/list-orders.md) | `POST /seller/api/v-1-0/get-orders` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [List Orders By Email](actions/list-orders-by-email.md) | `POST /seller/api/v-1-0/get-orders-by-email` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [List Products](actions/list-products.md) | `POST /seller/api/v-1-0/get-products` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
| [Update Product](actions/update-product.md) | `POST /seller/api/v-1-0/set-product` | [docs](https://my.sellty.ru/seller/docs/api-docs.json) |
