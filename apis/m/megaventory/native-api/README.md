# Megaventory: Native API Reference

A consolidated summary of Megaventory's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.megaventory.com/v2017a/metadata
- **API base URL:** `https://api.megaventory.com/v2017a`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.megaventory.com/en/articles/11382998-adding-an-api-key-to-your-user-account)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update Purchase Orders](actions/bulk-update-purchase-orders.md) | `POST /json/reply/PurchaseOrdersUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrdersUpdate) |
| [Bulk Update Sales Orders](actions/bulk-update-sales-orders.md) | `POST /json/reply/SalesOrdersUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrdersUpdate) |
| [Bulk Update Sales Quotes](actions/bulk-update-sales-quotes.md) | `POST /json/reply/SalesQuotesUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesQuotesUpdate) |
| [Cancel Purchase Order](actions/cancel-purchase-order.md) | `POST /json/reply/PurchaseOrderCancel` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrderCancel) |
| [Cancel Sales Order](actions/cancel-sales-order.md) | `POST /json/reply/SalesOrderCancel` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrderCancel) |
| [Get Product Pricing](actions/get-product-pricing.md) | `POST /json/reply/ProductPriceGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductPriceGet) |
| [List Contact Persons](actions/list-contact-persons.md) | `POST /json/reply/ContactPersonGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ContactPersonGet) |
| [List Inventory Levels](actions/list-inventory-levels.md) | `POST /json/reply/InventoryLocationStockGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationStockGet) |
| [List Inventory Locations](actions/list-inventory-locations.md) | `POST /json/reply/InventoryLocationGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationGet) |
| [List Product Categories](actions/list-product-categories.md) | `POST /json/reply/ProductCategoryGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductCategoryGet) |
| [List Product Clients](actions/list-product-clients.md) | `POST /json/reply/ProductClientGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductClientGet) |
| [List Product Suppliers](actions/list-product-suppliers.md) | `POST /json/reply/ProductSupplierGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductSupplierGet) |
| [List Products](actions/list-products.md) | `POST /json/reply/ProductGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductGet) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST /json/reply/PurchaseOrderGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrderGet) |
| [List Sales Orders](actions/list-sales-orders.md) | `POST /json/reply/SalesOrderGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrderGet) |
| [List Sales Quotes](actions/list-sales-quotes.md) | `POST /json/reply/SalesQuoteGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesQuoteGet) |
| [List Supplier Stock](actions/list-supplier-stock.md) | `POST /json/reply/SupplierStockGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SupplierStockGet) |
| [List Suppliers and Clients](actions/list-suppliers-and-clients.md) | `POST /json/reply/SupplierClientGet` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SupplierClientGet) |
| [Update Contact Person](actions/update-contact-person.md) | `POST /json/reply/ContactPersonUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ContactPersonUpdate) |
| [Update Inventory Levels](actions/update-inventory-levels.md) | `POST /json/reply/InventoryLocationStockProductStockUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationStockProductStockUpdate) |
| [Update Inventory Location](actions/update-inventory-location.md) | `POST /json/reply/InventoryLocationUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationUpdate) |
| [Update Product](actions/update-product.md) | `POST /json/reply/ProductUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductUpdate) |
| [Update Product Category](actions/update-product-category.md) | `POST /json/reply/ProductCategoryUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductCategoryUpdate) |
| [Update Product Client](actions/update-product-client.md) | `POST /json/reply/ProductClientUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductClientUpdate) |
| [Update Product Supplier](actions/update-product-supplier.md) | `POST /json/reply/ProductSupplierUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=ProductSupplierUpdate) |
| [Update Purchase Order](actions/update-purchase-order.md) | `POST /json/reply/PurchaseOrderUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrderUpdate) |
| [Update Sales Order](actions/update-sales-order.md) | `POST /json/reply/SalesOrderUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrderUpdate) |
| [Update Sales Quote](actions/update-sales-quote.md) | `POST /json/reply/SalesQuoteUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SalesQuoteUpdate) |
| [Update Supplier or Client](actions/update-supplier-or-client.md) | `POST /json/reply/SupplierClientUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SupplierClientUpdate) |
| [Update Supplier Stock](actions/update-supplier-stock.md) | `POST /json/reply/SupplierStockUpdate` | [docs](https://api.megaventory.com/v2017a/json/metadata?op=SupplierStockUpdate) |
