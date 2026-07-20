# Zydon: Native API Reference

A consolidated summary of Zydon's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.zydon.com.br/api-reference
- **OpenAPI specification:** https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FPSLb7DtcuAqWIRHDBT7b%2Fimports%2Fiymc1EHvBi0bellZxkhg%2Fswagger.json?alt=media&token=0de5ee09-fd2b-46ff-b37a-b76a2fb38bf4
- **API base URL:** `https://api.zydon.com.br/api/sales`

## Authentication

### Access Key Pair

Authenticate Zydon requests with the X-Zydon-Access-Key-Code and X-Zydon-Access-Key-Token headers.

### Credentials

- **Access Key Token:** `accessKeyToken` · required · The access-key token header value from Zydon.
- **Access Key Code:** `accessKeyCode` · required · The access-key code header value from Zydon.

Send these headers with each API request:

```http
X-Zydon-Access-Key-Code: <accessKeyCode>
X-Zydon-Access-Key-Token: <accessKeyToken>
```

[Official authentication documentation](https://docs.zydon.com.br/api-reference)

## Pagination

Use `perPage` in the query string to set the page size (default 25; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Brand](actions/get-brand.md) | `GET /brands/{id}` | [docs](https://docs.zydon.com.br/produtos/brands) |
| [Get Category](actions/get-category.md) | `GET /categories/{id}` | [docs](https://docs.zydon.com.br/produtos/categories) |
| [Get Company](actions/get-company.md) | `GET /companies/{id}` | [docs](https://docs.zydon.com.br/cadastros-gerais/companies) |
| [Get Measure Unit](actions/get-measure-unit.md) | `GET /measure-units/{id}` | [docs](https://docs.zydon.com.br/produtos/measure-units) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://docs.zydon.com.br/pedidos/orders) |
| [Get Partner](actions/get-partner.md) | `GET /partners/{id}` | [docs](https://docs.zydon.com.br/cadastros-gerais/partners) |
| [Get Payment Method](actions/get-payment-method.md) | `GET /payment-methods/{id}` | [docs](https://docs.zydon.com.br/pedidos/payment-methods) |
| [Get Price Table](actions/get-price-table.md) | `GET /price-tables/{id}` | [docs](https://docs.zydon.com.br/produtos/price-tables) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://docs.zydon.com.br/produtos/products) |
| [Get Profile](actions/get-profile.md) | `GET /profiles/{id}` | [docs](https://docs.zydon.com.br/cadastros-gerais/profiles) |
| [Get Sale](actions/get-sale.md) | `GET /sales/{id}` | [docs](https://docs.zydon.com.br/pedidos/sales) |
| [Get Seller](actions/get-seller.md) | `GET /sellers/{id}` | [docs](https://docs.zydon.com.br/cadastros-gerais/sellers) |
| [Get Variation](actions/get-variation.md) | `GET /variations/{id}` | [docs](https://docs.zydon.com.br/produtos/variations) |
| [Get Warehouse](actions/get-warehouse.md) | `GET /warehouses/{id}` | [docs](https://docs.zydon.com.br/produtos/warehouses) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://docs.zydon.com.br/produtos/brands) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://docs.zydon.com.br/produtos/categories) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://docs.zydon.com.br/cadastros-gerais/companies) |
| [List Financials](actions/list-financials.md) | `GET /financials` | [docs](https://docs.zydon.com.br/financeiro/financials) |
| [List Financials By Order](actions/list-financials-by-order.md) | `GET /financials/order/{orderId}` | [docs](https://docs.zydon.com.br/financeiro/financials/order) |
| [List Measure Units](actions/list-measure-units.md) | `GET /measure-units` | [docs](https://docs.zydon.com.br/produtos/measure-units) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://docs.zydon.com.br/pedidos/orders) |
| [List Partners](actions/list-partners.md) | `GET /partners` | [docs](https://docs.zydon.com.br/cadastros-gerais/partners) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /payment-methods` | [docs](https://docs.zydon.com.br/pedidos/payment-methods) |
| [List Price Tables](actions/list-price-tables.md) | `GET /price-tables` | [docs](https://docs.zydon.com.br/produtos/price-tables) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://docs.zydon.com.br/produtos/products) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://docs.zydon.com.br/cadastros-gerais/profiles) |
| [List Sales](actions/list-sales.md) | `GET /sales` | [docs](https://docs.zydon.com.br/pedidos/sales) |
| [List Sellers](actions/list-sellers.md) | `GET /sellers` | [docs](https://docs.zydon.com.br/cadastros-gerais/sellers) |
| [List Variations](actions/list-variations.md) | `GET /variations` | [docs](https://docs.zydon.com.br/produtos/variations) |
| [List Warehouses](actions/list-warehouses.md) | `GET /warehouses` | [docs](https://docs.zydon.com.br/produtos/warehouses) |
