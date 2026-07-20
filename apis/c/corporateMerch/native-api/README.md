# Corporate Merch: Native API Reference

A consolidated summary of Corporate Merch's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://corporatemerch.readme.io/reference
- **API base URL:** `https://api.corporatemerch.com`

## Authentication

### API Key

Use a Corporate Merch API token generated from Developers > API Tokens in the Corporate Merch dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://corporatemerch.readme.io/reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 15; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Designs To Organization](actions/assign-designs-to-organization.md) | `POST /v2/organizations/{organization}/designs` | [docs](https://corporatemerch.readme.io/reference/assign-design-to-organization) |
| [Cancel Order](actions/cancel-order.md) | `POST /v2/orders/{id}/cancel` | [docs](https://corporatemerch.readme.io/reference/cancel-an-order) |
| [Create Design](actions/create-design.md) | `POST /v2/designs` | [docs](https://corporatemerch.readme.io/reference/customize-product) |
| [Create Order](actions/create-order.md) | `POST /v2/orders` | [docs](https://corporatemerch.readme.io/reference/create-orders) |
| [Create Organization](actions/create-organization.md) | `POST /v2/organizations` | [docs](https://corporatemerch.readme.io/reference/create-organization) |
| [Customize Product](actions/customize-product.md) | `POST /v2/designs/customize` | [docs](https://corporatemerch.readme.io/reference/customize-a-product) |
| [Customize Product Async](actions/customize-product-async.md) | `POST /v2/designs/customize_async` | [docs](https://corporatemerch.readme.io/reference/customize-a-product-async) |
| [Delete Design](actions/delete-design.md) | `DELETE /v2/designs/{id}` | [docs](https://corporatemerch.readme.io/reference/delete-a-design) |
| [Get Catalog By Id](actions/get-catalog-by-id.md) | `GET /v2/catalog/{id}` | [docs](https://corporatemerch.readme.io/reference/get-catalog-by-id) |
| [Get Catalog Estimated Ship Date](actions/get-catalog-estimated-ship-date.md) | `GET /v2/catalog/{id}/estimated-ship-date` | [docs](https://corporatemerch.readme.io/reference/get-a-catalogs-estimated-ship-date) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /v2/wallets` | [docs](https://corporatemerch.readme.io/reference/get-credit-balance) |
| [Get Design By Id](actions/get-design-by-id.md) | `GET /v2/designs/{id}` | [docs](https://corporatemerch.readme.io/reference/get-design-by-id) |
| [Get Design Estimated Ship Date](actions/get-design-estimated-ship-date.md) | `GET /v2/designs/{id}/estimated-ship-date` | [docs](https://corporatemerch.readme.io/reference/get-designs-estimated-ship-date) |
| [Get Order By Id](actions/get-order-by-id.md) | `GET /v2/orders/{id}` | [docs](https://corporatemerch.readme.io/reference/get-order-by-id) |
| [Get Order Quote](actions/get-order-quote.md) | `POST /v2/orders/quote` | [docs](https://corporatemerch.readme.io/reference/get-order-quote) |
| [Get Shipment By Id](actions/get-shipment-by-id.md) | `GET /v2/orders/{order_id}/shipments/{shipment_id}` | [docs](https://corporatemerch.readme.io/reference/get-shipment-by-id) |
| [List Catalog](actions/list-catalog.md) | `GET /v2/catalog` | [docs](https://corporatemerch.readme.io/reference/list-catalog) |
| [List Designs](actions/list-designs.md) | `GET /v2/designs` | [docs](https://corporatemerch.readme.io/reference/list-designs) |
| [List Order Shipments](actions/list-order-shipments.md) | `GET /v2/orders/{id}/shipments` | [docs](https://corporatemerch.readme.io/reference/list-order-shipments) |
| [List Orders](actions/list-orders.md) | `GET /v2/orders` | [docs](https://corporatemerch.readme.io/reference/list-orders) |
| [List Organization Designs](actions/list-organization-designs.md) | `GET /v2/organizations/{organization}/designs` | [docs](https://corporatemerch.readme.io/reference/retreive-list-of-designs-for-given-organization) |
| [List Organizations](actions/list-organizations.md) | `GET /v2/organizations` | [docs](https://corporatemerch.readme.io/reference/list-organizations) |
| [Update Customized Product](actions/update-customized-product.md) | `POST /v2/designs/customize/{id}` | [docs](https://corporatemerch.readme.io/reference/update-customized-product) |
| [Update Order Address](actions/update-order-address.md) | `PUT /v2/orders/{id}/update_address` | [docs](https://corporatemerch.readme.io/reference/update-an-order-address) |
| [Update Organization](actions/update-organization.md) | `PUT /v2/organizations/{organization}` | [docs](https://corporatemerch.readme.io/reference/update-organization) |
