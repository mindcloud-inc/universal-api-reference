# Everbill: Native API Reference

A consolidated summary of Everbill's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://api.everbill.eu/
- **OpenAPI specification:** https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json
- **API base URL:** `https://api.everbill.eu`

## Authentication

### Email/password bearer token

Sign in with an Everbill email and password to obtain a bearer token for API requests.

### Credentials

- **Email:** `email` · required · Everbill login email used by the documented sign-in endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.paging.pageCount`. The current page number is read from `data.paging.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Bill Item](actions/add-bill-item.md) | `POST /bills/add_item/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1add_item~1{id}/post) |
| [Add Bill Transaction](actions/add-bill-transaction.md) | `POST /bills/add_transaction/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1add_transaction~1{id}/post) |
| [Add Offer Item](actions/add-offer-item.md) | `POST /offers/add_item/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1add_item~1{id}/post) |
| [Add Order Item](actions/add-order-item.md) | `POST /orders/add_item/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1add_item~1{id}/post) |
| [Create Article](actions/create-article.md) | `POST /articles/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1articles~1add/post) |
| [Create Article Category](actions/create-article-category.md) | `POST /article_categories/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1article_categories~1add/post) |
| [Create Bill](actions/create-bill.md) | `POST /bills/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1add/post) |
| [Create Cost Unit](actions/create-cost-unit.md) | `POST /cost_units/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1cost_units~1add/post) |
| [Create Customer](actions/create-customer.md) | `POST /customers/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1customers~1add/post) |
| [Create Distributor](actions/create-distributor.md) | `POST /distributors/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1distributors~1add/post) |
| [Create Incoming Bill](actions/create-incoming-bill.md) | `POST /incoming_bills/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1incoming_bills~1add/post) |
| [Create Offer](actions/create-offer.md) | `POST /offers/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1add/post) |
| [Create Order](actions/create-order.md) | `POST /orders/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1add/post) |
| [Create Project](actions/create-project.md) | `POST /projects/add` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1projects~1add/post) |
| [Get Article](actions/get-article.md) | `GET /articles/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1articles~1view~1{id}/get) |
| [Get Bill](actions/get-bill.md) | `GET /bills/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1view~1{id}/get) |
| [Get Cost Unit](actions/get-cost-unit.md) | `GET /cost_units/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1cost_units~1view~1{id}/get) |
| [Get Customer](actions/get-customer.md) | `GET /customers/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1customers~1view~1{id}/get) |
| [Get Distributor](actions/get-distributor.md) | `GET /distributors/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1distributors~1view~1{id}/get) |
| [Get Document PDF](actions/get-document-pdf.md) | `GET /:document_name/get_pdf/:document_number` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1{document_name}~1get_pdf~1{document_number}/get) |
| [Get Incoming Bill](actions/get-incoming-bill.md) | `GET /incoming_bills/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1incoming_bills~1view~1{id}/get) |
| [Get Offer](actions/get-offer.md) | `GET /offers/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1view~1{id}/get) |
| [Get Order](actions/get-order.md) | `GET /orders/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1view~1{id}/get) |
| [Get Project](actions/get-project.md) | `GET /projects/view/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1projects~1view~1{id}/get) |
| [List Article Categories](actions/list-article-categories.md) | `GET /article_categories/threaded` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1article_categories~1threaded/get) |
| [List Articles](actions/list-articles.md) | `GET /articles/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json) |
| [List Bills](actions/list-bills.md) | `GET /bills/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1index/get) |
| [List Cost Units](actions/list-cost-units.md) | `GET /cost_units/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1cost_units~1index/get) |
| [List Customers](actions/list-customers.md) | `GET /customers/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1customers~1index/get) |
| [List Distributors](actions/list-distributors.md) | `GET /distributors/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1distributors~1index/get) |
| [List Incoming Bills](actions/list-incoming-bills.md) | `GET /incoming_bills/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1incoming_bills~1index/get) |
| [List Offers](actions/list-offers.md) | `GET /offers/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1index/get) |
| [List Orders](actions/list-orders.md) | `GET /orders/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1index/get) |
| [List Projects](actions/list-projects.md) | `GET /projects/index` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1projects~1index/get) |
| [Sign In](actions/sign-in.md) | `POST /signin` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json) |
| [Update Article](actions/update-article.md) | `PUT /articles/update/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1articles~1update{id}/put) |
| [Update Bill](actions/update-bill.md) | `PUT /bills/update/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1update~1{id}/put) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/update/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1customers~1update~1{id}/put) |
| [Update Distributor](actions/update-distributor.md) | `PUT /distributors/update/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1distributors~1update~1{id}/put) |
| [Update Offer](actions/update-offer.md) | `PUT /offers/update/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1update~1{id}/put) |
| [Update Order](actions/update-order.md) | `PUT /orders/update/:id` | [docs](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1update~1{id}/put) |
