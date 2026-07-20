# Loyverse: Native API Reference

A consolidated summary of Loyverse's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.loyverse.com/docs/
- **OpenAPI specification:** https://developer.loyverse.com/docs/API-Reference__v1.0.yaml
- **API base URL:** `https://api.loyverse.com/v1.0`

## Authentication

### Personal Access Token

Use a Loyverse personal access token to access one merchant account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.loyverse.com/docs/#section/Authorization/Personal-access-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–250). Use `cursor` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Update Inventory Levels](actions/batch-update-inventory-levels.md) | `POST /inventory` | [docs](https://developer.loyverse.com/docs/#tag/Inventory) |
| [Create or Update Category](actions/create-or-update-category.md) | `POST /categories` | [docs](https://developer.loyverse.com/docs/#tag/Categories) |
| [Create or Update Customer](actions/create-or-update-customer.md) | `POST /customers` | [docs](https://developer.loyverse.com/docs/#tag/Customers) |
| [Create or Update Item](actions/create-or-update-item.md) | `POST /items` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [Create or Update Supplier](actions/create-or-update-supplier.md) | `POST /suppliers/` | [docs](https://developer.loyverse.com/docs/#tag/Suppliers) |
| [Create or Update Variant](actions/create-or-update-variant.md) | `POST /variants` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [Create Refund Receipt](actions/create-refund-receipt.md) | `POST /receipts/:receipt_number/refund` | [docs](https://developer.loyverse.com/docs/#tag/Receipts) |
| [Create Sales Receipt](actions/create-sales-receipt.md) | `POST /receipts` | [docs](https://developer.loyverse.com/docs/#tag/Receipts) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:category_id` | [docs](https://developer.loyverse.com/docs/#tag/Categories) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:customer_id` | [docs](https://developer.loyverse.com/docs/#tag/Customers) |
| [Delete Item](actions/delete-item.md) | `DELETE /items/:item_id` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [Delete Supplier](actions/delete-supplier.md) | `DELETE /suppliers/:supplier_id` | [docs](https://developer.loyverse.com/docs/#tag/Suppliers) |
| [Delete Variant](actions/delete-variant.md) | `DELETE /variants/:variant_id` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [Get Category](actions/get-category.md) | `GET /categories/:category_id` | [docs](https://developer.loyverse.com/docs/#tag/Categories) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customer_id` | [docs](https://developer.loyverse.com/docs/#tag/Customers) |
| [Get Item](actions/get-item.md) | `GET /items/:item_id` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [Get Receipt](actions/get-receipt.md) | `GET /receipts/:receipt_number` | [docs](https://developer.loyverse.com/docs/#tag/Receipts) |
| [Get Shift](actions/get-shift.md) | `GET /shifts/:shift_id` | [docs](https://developer.loyverse.com/docs/#tag/Shifts) |
| [Get Store](actions/get-store.md) | `GET /stores/:store_id` | [docs](https://developer.loyverse.com/docs/#tag/Stores) |
| [Get Supplier](actions/get-supplier.md) | `GET /suppliers/:supplier_id` | [docs](https://developer.loyverse.com/docs/#tag/Suppliers) |
| [Get Variant](actions/get-variant.md) | `GET /variants/:variant_id` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developer.loyverse.com/docs/#tag/Categories) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developer.loyverse.com/docs/#tag/Customers) |
| [List Inventory Levels](actions/list-inventory-levels.md) | `GET /inventory` | [docs](https://developer.loyverse.com/docs/#tag/Inventory) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
| [List Receipts](actions/list-receipts.md) | `GET /receipts` | [docs](https://developer.loyverse.com/docs/#tag/Receipts) |
| [List Shifts](actions/list-shifts.md) | `GET /shifts` | [docs](https://developer.loyverse.com/docs/#tag/Shifts) |
| [List Stores](actions/list-stores.md) | `GET /stores` | [docs](https://developer.loyverse.com/docs/#tag/Stores) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers/` | [docs](https://developer.loyverse.com/docs/#tag/Suppliers) |
| [List Variants](actions/list-variants.md) | `GET /variants` | [docs](https://developer.loyverse.com/docs/#tag/Items) |
