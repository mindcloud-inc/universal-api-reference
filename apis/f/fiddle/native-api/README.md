# Fiddle: Native API Reference

A consolidated summary of Fiddle's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://fiddle.io/rest/api/v2/docs/
- **OpenAPI specification:** https://fiddle.io/rest/api/v2/openapi.json
- **API base URL:** `https://fiddle.io/rest/api/v2`

## Authentication

### API Key

Authenticate with a Fiddle API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://fiddle.io/rest/api/v2/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `inventoryTypes`.

## Pagination

Use `size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /purchase-orders` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Create Supplier](actions/create-supplier.md) | `POST /suppliers` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Find Customer by ID](actions/find-customer-by-id.md) | `GET /customers/:customerId` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Find Purchase Order by ID](actions/find-purchase-order-by-id.md) | `GET /purchase-orders/:purchaseOrderId` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Find Supplier by ID](actions/find-supplier-by-id.md) | `GET /suppliers/:supplierId` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /inventory-items` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Inventory Locations](actions/list-inventory-locations.md) | `GET /inventory-locations` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Inventory Lots](actions/list-inventory-lots.md) | `GET /inventory-lots` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Inventory Types](actions/list-inventory-types.md) | `GET /inventory-types` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Measurement Units](actions/list-measurement-units.md) | `GET /measurement-units` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /purchase-orders` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Quarantined Lots](actions/list-quarantined-lots.md) | `GET /inventory-lots/quarantine` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Sales Order Items](actions/list-sales-order-items.md) | `GET /sales-order-items` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /sales-orders` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [List Work Orders](actions/list-work-orders.md) | `GET /work-orders` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Update Purchase Order](actions/update-purchase-order.md) | `PUT /purchase-orders` | [docs](https://fiddle.io/rest/api/v2/docs/) |
| [Update Supplier](actions/update-supplier.md) | `PUT /supplier/:supplierId` | [docs](https://fiddle.io/rest/api/v2/docs/) |
