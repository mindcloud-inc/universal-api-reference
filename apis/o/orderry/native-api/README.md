# Orderry: Native API Reference

A consolidated summary of Orderry's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://orderry.readme.io/reference/getting-started
- **API base URL:** `https://api.orderry.com`

## Authentication

### API Key

Authenticate to Orderry with a personal API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://orderry.readme.io/reference/getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | `GET settings/company` | [docs](https://orderry.readme.io/reference/get-company-settings) |
| [Get Company Taxes](actions/get-company-taxes.md) | `GET settings/taxes` | [docs](https://orderry.readme.io/reference/get-company-taxes) |
| [Get Organization by ID](actions/get-organization-by-id.md) | `GET contacts/organizations/:organizationId` | [docs](https://orderry.readme.io/reference/get-organization-by-id) |
| [Get Person by ID](actions/get-person-by-id.md) | `GET contacts/people/:personId` | [docs](https://orderry.readme.io/reference/get-person-by-id) |
| [Get Product by ID](actions/get-product-by-id.md) | `GET products/:productId` | [docs](https://orderry.readme.io/reference/get-product-by-id) |
| [Get Service by ID](actions/get-service-by-id.md) | `GET services/:serviceId` | [docs](https://orderry.readme.io/reference/get-service-by-id) |
| [List Ad Campaigns](actions/list-ad-campaigns.md) | `GET marketing/campaigns/` | [docs](https://orderry.readme.io/reference/get-ad-campaigns) |
| [List Asset Custom Fields](actions/list-asset-custom-fields.md) | `GET warehouse/assets/custom-fields/` | [docs](https://orderry.readme.io/reference/get-asset-custom-fields) |
| [List Asset Directories](actions/list-asset-directories.md) | `GET warehouse/assets/directories` | [docs](https://orderry.readme.io/reference/get-directories-of-assets) |
| [List Assets](actions/list-assets.md) | `GET warehouse/assets` | [docs](https://orderry.readme.io/reference/get-assets) |
| [List Bookings](actions/list-bookings.md) | `GET bookings` | [docs](https://orderry.readme.io/reference/get-bookings) |
| [List Cashbox Transactions](actions/list-cashbox-transactions.md) | `GET cashbox/report/:cashboxId` | [docs](https://orderry.readme.io/reference/get-cashbox-transactions) |
| [List Cashboxes](actions/list-cashboxes.md) | `GET cashbox/` | [docs](https://orderry.readme.io/reference/get-cashboxes) |
| [List Employees](actions/list-employees.md) | `GET employees/` | [docs](https://orderry.readme.io/reference/get-employees) |
| [List Estimate Statuses](actions/list-estimate-statuses.md) | `GET statuses/estimates` | [docs](https://orderry.readme.io/reference/get-estimate-statuses) |
| [List Estimates](actions/list-estimates.md) | `GET estimates` | [docs](https://orderry.readme.io/reference/get-estimates) |
| [List Inventory Postings](actions/list-inventory-postings.md) | `GET warehouse/postings/` | [docs](https://orderry.readme.io/reference/get-inventory-postings) |
| [List Inventory Transfers](actions/list-inventory-transfers.md) | `GET warehouse/moves/` | [docs](https://orderry.readme.io/reference/get-inventory-transfers) |
| [List Inventory Write-Offs](actions/list-inventory-write-offs.md) | `GET warehouse/outcome-transactions/` | [docs](https://orderry.readme.io/reference/get-inventory-writeoffs) |
| [List Invoice Statuses](actions/list-invoice-statuses.md) | `GET statuses/invoices` | [docs](https://orderry.readme.io/reference/get-invoice-statuses) |
| [List Invoices](actions/list-invoices.md) | `GET invoice/` | [docs](https://orderry.readme.io/reference/get-invoices) |
| [List Lead Custom Fields](actions/list-lead-custom-fields.md) | `GET lead/custom-fields/` | [docs](https://orderry.readme.io/reference/get-lead-custom-fields) |
| [List Lead Statuses](actions/list-lead-statuses.md) | `GET statuses/leads` | [docs](https://orderry.readme.io/reference/get-lead-statuses) |
| [List Lead Types](actions/list-lead-types.md) | `GET lead/types/` | [docs](https://orderry.readme.io/reference/get-lead-types) |
| [List Leads](actions/list-leads.md) | `GET lead/` | [docs](https://orderry.readme.io/reference/get-leads) |
| [List Location Resources](actions/list-location-resources.md) | `GET branches/resources/` | [docs](https://orderry.readme.io/reference/get-location-resources) |
| [List Locations](actions/list-locations.md) | `GET branches/` | [docs](https://orderry.readme.io/reference/get-locations) |
| [List Order Custom Fields](actions/list-order-custom-fields.md) | `GET orders/custom-fields` | [docs](https://orderry.readme.io/reference/get-orderestimate-custom-fields) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET statuses/orders` | [docs](https://orderry.readme.io/reference/get-order-statuses) |
| [List Order Types](actions/list-order-types.md) | `GET orders/types` | [docs](https://orderry.readme.io/reference/get-orderestimate-types) |
| [List Orders](actions/list-orders.md) | `GET orders` | [docs](https://orderry.readme.io/reference/get-orders) |
| [List Organization People](actions/list-organization-people.md) | `GET contacts/organizations/:organizationId/people` | [docs](https://orderry.readme.io/reference/get-organization-people) |
| [List Organizations](actions/list-organizations.md) | `GET contacts/organizations` | [docs](https://orderry.readme.io/reference/get-organizations) |
| [List People](actions/list-people.md) | `GET contacts/people` | [docs](https://orderry.readme.io/reference/get-people) |
| [List Person Organizations](actions/list-person-organizations.md) | `GET contacts/people/:personId/organizations` | [docs](https://orderry.readme.io/reference/get-person-organization) |
| [List Prices](actions/list-prices.md) | `GET margins/` | [docs](https://orderry.readme.io/reference/get-prices) |
| [List Product Categories](actions/list-product-categories.md) | `GET warehouse/categories/` | [docs](https://orderry.readme.io/reference/get-product-categories) |
| [List Products](actions/list-products.md) | `GET products/` | [docs](https://orderry.readme.io/reference/get-products) |
| [List Sales](actions/list-sales.md) | `GET retail/sales/` | [docs](https://orderry.readme.io/reference/get-sales) |
| [List Service Categories](actions/list-service-categories.md) | `GET services/categories/` | [docs](https://orderry.readme.io/reference/get-service-categories) |
| [List Services](actions/list-services.md) | `GET services/` | [docs](https://orderry.readme.io/reference/get-service) |
| [List Stock](actions/list-stock.md) | `GET warehouse/goods/:warehouseId` | [docs](https://orderry.readme.io/reference/get-stock) |
| [List Units of Measurement](actions/list-units-of-measurement.md) | `GET catalogs/uoms` | [docs](https://orderry.readme.io/reference/get-units-of-measurement) |
| [List Warehouse Bins](actions/list-warehouse-bins.md) | `GET warehouse/:warehouseId/cells` | [docs](https://orderry.readme.io/reference/get-warehouse-bins) |
| [List Warehouses](actions/list-warehouses.md) | `GET warehouse/` | [docs](https://orderry.readme.io/reference/get-warehouses) |
