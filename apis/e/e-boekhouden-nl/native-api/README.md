# e-Boekhouden.nl: Native API Reference

A consolidated summary of e-Boekhouden.nl's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://api.e-boekhouden.nl/swagger/index.html
- **OpenAPI specification:** https://api.e-boekhouden.nl/swagger/v1/swagger.json
- **REST API base URL:** `https://api.e-boekhouden.nl`
- **REST API base URL:** `https://api.e-boekhouden.nl`

## Authentication

### API Token

Exchange an e-Boekhouden API token for a short-lived session token before running requests.

### Credentials

- **API Token:** `apiToken` · required · API token from the e-Boekhouden account settings page.

Send these headers with each API request:

```http
Authorization: <custom.token>
```

[Official authentication documentation](https://api.e-boekhouden.nl/swagger/index.html)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### REST API

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Pagination

- **REST API:** Use `limit` in the query string to set the page size (default 100; accepted range 1–2000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Cost Center](actions/create-cost-center.md) | `POST /v1/costcenter` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Create Invoice](actions/create-invoice.md) | `POST /v1/invoice` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Create Ledger](actions/create-ledger.md) | `POST /v1/ledger` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Create Member](actions/create-member.md) | `POST /v1/member` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Create Mutation](actions/create-mutation.md) | `POST /v1/mutation` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Create Product](actions/create-product.md) | `POST /v1/product` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Create Relation](actions/create-relation.md) | `POST /v1/relation` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Delete Cost Center](actions/delete-cost-center.md) | `DELETE /v1/costcenter/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Delete Product](actions/delete-product.md) | `DELETE /v1/product/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Cost Center](actions/get-cost-center.md) | `GET /v1/costcenter/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Invoice](actions/get-invoice.md) | `GET /v1/invoice/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Ledger](actions/get-ledger.md) | `GET /v1/ledger/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Ledger Balance](actions/get-ledger-balance.md) | `GET /v1/ledger/:id/balance` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Member](actions/get-member.md) | `GET /v1/member/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Mutation](actions/get-mutation.md) | `GET /v1/mutation/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Product](actions/get-product.md) | `GET /v1/product/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Get Relation](actions/get-relation.md) | `GET /v1/relation/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Administrations](actions/list-administrations.md) | `GET /v1/administration` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Cost Centers](actions/list-cost-centers.md) | `GET /v1/costcenter` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Email Templates](actions/list-email-templates.md) | `GET /v1/emailtemplate` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Invoice Templates](actions/list-invoice-templates.md) | `GET /v1/invoicetemplate` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Invoices](actions/list-invoices.md) | `GET /v1/invoice` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Ledgers](actions/list-ledgers.md) | `GET /v1/ledger` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Linked Administrations](actions/list-linked-administrations.md) | `GET /v1/administration/linked` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Members](actions/list-members.md) | `GET /v1/member` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Mutations](actions/list-mutations.md) | `GET /v1/mutation` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Outstanding Invoices](actions/list-outstanding-invoices.md) | `GET /v1/mutation/invoice/outstanding` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Product Groups](actions/list-product-groups.md) | `GET /v1/product/groups` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Products](actions/list-products.md) | `GET /v1/product` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Relations](actions/list-relations.md) | `GET /v1/relation` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [List Units](actions/list-units.md) | `GET /v1/unit` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Update Cost Center](actions/update-cost-center.md) | `PATCH /v1/costcenter/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Update Ledger](actions/update-ledger.md) | `PATCH /v1/ledger/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Update Member](actions/update-member.md) | `PATCH /v1/member/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Update Product](actions/update-product.md) | `PATCH /v1/product/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
| [Update Relation](actions/update-relation.md) | `PATCH /v1/relation/:id` | [docs](https://api.e-boekhouden.nl/swagger/index.html) |
