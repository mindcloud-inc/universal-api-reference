# <img src="https://images.mindcloud.co/apps/icons/in-flow-inventory_1774547377487.png" alt="inFlow Inventory logo" width="28" height="28"> inFlow Inventory: Universal API

Inventory and order management for products, customers, vendors, purchasing, and stock movement in inFlow Inventory.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inFlowInventory/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.inflowinventory.com
- **Vendor API docs:** https://cloudapi.inflowinventory.com/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves an existing customer from inFlow Inventory. |
| [Insert or Update Customer](actions/insert-or-update-customer.md) | PUT | Inserts or updates a customer in inFlow Inventory. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from inFlow Inventory. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Inventory Summary](actions/get-product-inventory-summary.md) | GET | Retrieves a product inventory summary from inFlow Inventory. |
| [List Multiple Product Inventory Summaries](actions/list-multiple-product-inventory-summaries.md) | GET | Retrieves multiple product inventory summaries from inFlow Inventory. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves an existing location from inFlow Inventory. |
| [List Locations](actions/list-locations.md) | GET | Retrieves location records from inFlow Inventory. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves an existing product from inFlow Inventory. |
| [Insert or Update Product](actions/insert-or-update-product.md) | PUT | Inserts or updates a product in inFlow Inventory. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from inFlow Inventory. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves an existing purchase order from inFlow Inventory. |
| [Insert or Update Purchase Order](actions/insert-or-update-purchase-order.md) | PUT | Inserts or updates a purchase order in inFlow Inventory. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from inFlow Inventory. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves an existing sales order from inFlow Inventory. |
| [Insert or Update Sales Order](actions/insert-or-update-sales-order.md) | PUT | Inserts or updates a sales order in inFlow Inventory. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from inFlow Inventory. |

### Stock Movements

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Adjustment](actions/get-stock-adjustment.md) | GET | Retrieves an existing stock adjustment from inFlow Inventory. |
| [Get Stock Transfer](actions/get-stock-transfer.md) | GET | Retrieves an existing stock transfer from inFlow Inventory. |
| [Insert or Update Stock Transfer](actions/insert-or-update-stock-transfer.md) | PUT | Inserts or updates a stock transfer in inFlow Inventory. |
| [List Stock Adjustments](actions/list-stock-adjustments.md) | GET | Retrieves stock adjustments from inFlow Inventory. |
| [List Stock Transfers](actions/list-stock-transfers.md) | GET | Retrieves stock transfers from inFlow Inventory. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor](actions/get-vendor.md) | GET | Retrieves an existing vendor from inFlow Inventory. |
| [Insert or Update Vendor](actions/insert-or-update-vendor.md) | PUT | Inserts or updates a vendor in inFlow Inventory. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves vendor records from inFlow Inventory. |

