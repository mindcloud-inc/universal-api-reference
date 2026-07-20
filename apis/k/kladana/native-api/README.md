# Kladana: Native API Reference

A consolidated summary of Kladana's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://dev.kladana.com/doc/api/remap/1.2/
- **API base URL:** `https://api.kladana.com/api/remap/1.2`

## Authentication

### Basic Auth

HTTP Basic authentication using the Kladana account username and password. MindCloud builds the Basic Authorization header from the connection fields.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://dev.kladana.com/doc/api/remap/1.2/#authentication)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `like`, `lt`, `lte`, `neq`.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Advanced Stock Report](actions/get-advanced-stock-report.md) | `GET /report/stock/all` | [docs](https://dev.kladana.com/doc/api/remap/1.2/reports/#reports-stock-report-get-advanced-stock-report) |
| [Get Brief Stock Report](actions/get-brief-stock-report.md) | `GET /report/stock/all/current` | [docs](https://dev.kladana.com/doc/api/remap/1.2/reports/#reports-stock-report-get-the-brief-stock-report) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /context/companysettings` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-company-settings-get-company-settings) |
| [Get Company Subscription](actions/get-company-subscription.md) | `GET /accountSettings/subscription` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-company-subscription-get-company-subscription) |
| [Get Counterparty](actions/get-counterparty.md) | `GET /entity/counterparty/{id}` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-counterparty-get-counterparty) |
| [Get Counterparty Indicators](actions/get-counterparty-indicators.md) | `GET /report/counterparty` | [docs](https://dev.kladana.com/doc/api/remap/1.2/reports/#reports-report-indicators-of-counterparties-get-indicators-of-counterparties) |
| [Get Counterparty Metadata](actions/get-counterparty-metadata.md) | `GET /entity/counterparty/metadata` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-counterparty-metadata-of-counterparties) |
| [Get Current Employee Context](actions/get-current-employee-context.md) | `GET /context/employee` | [docs](https://dev.kladana.com/doc/api/remap/1.2/#employee-request-context) |
| [Get Product](actions/get-product.md) | `GET /entity/product/{id}` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-product-get-item) |
| [Get Product Directory Settings](actions/get-product-directory-settings.md) | `GET /entity/assortment/settings` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-assortment-get-product-directory-settings) |
| [Get Product Metadata](actions/get-product-metadata.md) | `GET /entity/product/metadata` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-product-item-metadata) |
| [Get Product Variant Metadata](actions/get-product-variant-metadata.md) | `GET /entity/variant/metadata` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-product-variant-product-variant-metadata) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /entity/customerorder/{id}` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-sales-order-get-sales-order) |
| [Get Service](actions/get-service.md) | `GET /entity/service/{id}` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-service-get-service) |
| [Get Shipment](actions/get-shipment.md) | `GET /entity/demand/{id}` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-shipment-get-shipment) |
| [List Assortment](actions/list-assortment.md) | `GET /entity/assortment` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-assortment-get-assortment) |
| [List Batches](actions/list-batches.md) | `GET /entity/consignment` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-batch-get-a-list-of-batches) |
| [List Bundles](actions/list-bundles.md) | `GET /entity/bundle` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-bundle-get-the-list-of-bundles) |
| [List Contracts](actions/list-contracts.md) | `GET /entity/contract` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-contract-get-a-list-of-contracts) |
| [List Counterparties](actions/list-counterparties.md) | `GET /entity/counterparty` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-counterparty-get-a-list-of-counterparties) |
| [List Countries](actions/list-countries.md) | `GET /entity/country` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-country-get-countries) |
| [List Currencies](actions/list-currencies.md) | `GET /entity/currency/` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-currency-get-currencies) |
| [List Employees](actions/list-employees.md) | `GET /entity/employee` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-employee-get-employees) |
| [List Incoming Payments](actions/list-incoming-payments.md) | `GET /entity/paymentin` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-incoming-payment-get-incoming-payments) |
| [List Inventory Counts](actions/list-inventory-counts.md) | `GET /entity/inventory` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-inventory-count-get-inventory-counts) |
| [List Organizations](actions/list-organizations.md) | `GET /entity/organization` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-entity-get-a-list-of-legal-entities) |
| [List Outgoing Payments](actions/list-outgoing-payments.md) | `GET /entity/paymentout` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-outgoing-payment-get-outgoing-payments) |
| [List Product Groups](actions/list-product-groups.md) | `GET /entity/productfolder` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-product-group-get-a-list-of-product-groups) |
| [List Product Variants](actions/list-product-variants.md) | `GET /entity/variant` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-product-variant-get-a-list-of-product-variants) |
| [List Products](actions/list-products.md) | `GET /entity/product` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-product-get-a-list-of-products) |
| [List Projects](actions/list-projects.md) | `GET /entity/project` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-project-get-projects) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /entity/purchaseorder` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-purchase-order-get-a-list-of-purchase-orders) |
| [List Receivings](actions/list-receivings.md) | `GET /entity/supply` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-receiving-get-list-of-receivings) |
| [List Sales Invoices](actions/list-sales-invoices.md) | `GET /entity/invoiceout` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-sales-invoice-get-sales-invoices) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /entity/customerorder` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-sales-order-get-the-list-of-sales-orders) |
| [List Services](actions/list-services.md) | `GET /entity/service` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-service-get-a-list-of-services) |
| [List Shipments](actions/list-shipments.md) | `GET /entity/demand` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-shipment-get-a-list-of-shipments) |
| [List Supplier Invoices](actions/list-supplier-invoices.md) | `GET /entity/invoicein` | [docs](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-supplier-invoice-get-supplier-invoices) |
| [List Units Of Measure](actions/list-units-of-measure.md) | `GET /entity/uom` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-unit-of-measure-get-units-of-measure) |
| [List Warehouses](actions/list-warehouses.md) | `GET /entity/store` | [docs](https://dev.kladana.com/doc/api/remap/1.2/dictionaries/#entities-warehouse-get-warehouses) |
