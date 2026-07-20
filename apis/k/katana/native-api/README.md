# Katana: Native API Reference

A consolidated summary of Katana's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.katanamrp.com/reference
- **API base URL:** `https://api.katanamrp.com/v1`

## Authentication

### API Key

Use a Katana API key in the Authorization header for all requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://developer.katanamrp.com/reference/api-authentication)

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://developer.katanamrp.com/reference/create-customer) |
| [Create Manufacturing Order](actions/create-manufacturing-order.md) | `POST /manufacturing_orders` | [docs](https://developer.katanamrp.com/reference/createmanufacturingorder) |
| [Create Material](actions/create-material.md) | `POST /materials` | [docs](https://developer.katanamrp.com/reference/creatematerial) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://developer.katanamrp.com/reference/create-product) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /purchase_orders` | [docs](https://developer.katanamrp.com/reference/createpurchaseorder) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /sales_orders` | [docs](https://developer.katanamrp.com/reference/create-sales-order) |
| [Create Sales Order Fulfillment](actions/create-sales-order-fulfillment.md) | `POST /sales_order_fulfillments` | [docs](https://developer.katanamrp.com/reference/create-sales-order-fulfillment) |
| [Create Supplier](actions/create-supplier.md) | `POST /suppliers` | [docs](https://developer.katanamrp.com/reference/create-supplier) |
| [Create Variant](actions/create-variant.md) | `POST /variants` | [docs](https://developer.katanamrp.com/reference/create-variant) |
| [List Current Inventory](actions/list-current-inventory.md) | `GET /inventory` | [docs](https://developer.katanamrp.com/reference/list-current-inventory) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developer.katanamrp.com/reference/list-all-customers) |
| [List Inventory Movements](actions/list-inventory-movements.md) | `GET /inventory_movements` | [docs](https://developer.katanamrp.com/reference/list-all-inventory-movements) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://developer.katanamrp.com/reference/list-all-locations) |
| [List Manufacturing Orders](actions/list-manufacturing-orders.md) | `GET /manufacturing_orders` | [docs](https://developer.katanamrp.com/reference/getallmanufacturingorders) |
| [List Materials](actions/list-materials.md) | `GET /materials` | [docs](https://developer.katanamrp.com/reference/getallmaterials) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developer.katanamrp.com/reference/list-all-products) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /purchase_orders` | [docs](https://developer.katanamrp.com/reference/findpurchaseorders) |
| [List Sales Order Fulfillments](actions/list-sales-order-fulfillments.md) | `GET /sales_order_fulfillments` | [docs](https://developer.katanamrp.com/reference/list-all-sales-order-fulfillments) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /sales_orders` | [docs](https://developer.katanamrp.com/reference/list-all-sales-orders) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers` | [docs](https://developer.katanamrp.com/reference/list-all-suppliers) |
| [List Variants](actions/list-variants.md) | `GET /variants` | [docs](https://developer.katanamrp.com/reference/list-all-variants) |
| [List Variants with Negative Stock](actions/list-variants-with-negative-stock.md) | `GET /negative_stock` | [docs](https://developer.katanamrp.com/reference/getallnegativestock) |
| [Receive Purchase Order](actions/receive-purchase-order.md) | `POST /purchase_order_receive` | [docs](https://developer.katanamrp.com/reference/receivepurchaseorder) |
| [Retrieve Current Factory](actions/retrieve-current-factory.md) | `GET /factory` | [docs](https://developer.katanamrp.com/reference/getfactory) |
| [Retrieve Manufacturing Order](actions/retrieve-manufacturing-order.md) | `GET /manufacturing_orders/:id` | [docs](https://developer.katanamrp.com/reference/getmanufacturingorder) |
| [Retrieve Material](actions/retrieve-material.md) | `GET /materials/:id` | [docs](https://developer.katanamrp.com/reference/getmaterial) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /products/:id` | [docs](https://developer.katanamrp.com/reference/getproduct) |
| [Retrieve Purchase Order](actions/retrieve-purchase-order.md) | `GET /purchase_orders/:id` | [docs](https://developer.katanamrp.com/reference/getpurchaseorder) |
| [Retrieve Sales Order](actions/retrieve-sales-order.md) | `GET /sales_orders/:id` | [docs](https://developer.katanamrp.com/reference/retrieve-sales-order) |
| [Retrieve Variant](actions/retrieve-variant.md) | `GET /variants/:id` | [docs](https://developer.katanamrp.com/reference/getvariant) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/:id` | [docs](https://developer.katanamrp.com/reference/updatecustomer) |
| [Update Manufacturing Order](actions/update-manufacturing-order.md) | `PATCH /manufacturing_orders/:id` | [docs](https://developer.katanamrp.com/reference/updatemanufacturingorder) |
| [Update Material](actions/update-material.md) | `PATCH /materials/:id` | [docs](https://developer.katanamrp.com/reference/updatematerial) |
| [Update Product](actions/update-product.md) | `PATCH /products/:id` | [docs](https://developer.katanamrp.com/reference/updateproduct) |
| [Update Purchase Order](actions/update-purchase-order.md) | `PATCH /purchase_orders/:id` | [docs](https://developer.katanamrp.com/reference/updatepurchaseorder) |
| [Update Reorder Point](actions/update-reorder-point.md) | `POST /inventory_reorder_points` | [docs](https://developer.katanamrp.com/reference/update-reorder-point) |
| [Update Safety Stock Level](actions/update-safety-stock-level.md) | `POST /inventory_safety_stock_levels` | [docs](https://developer.katanamrp.com/reference/createinventorysafetystocklevel) |
| [Update Sales Order](actions/update-sales-order.md) | `PATCH /sales_orders/:id` | [docs](https://developer.katanamrp.com/reference/update-sales-order) |
| [Update Supplier](actions/update-supplier.md) | `PATCH /suppliers/:id` | [docs](https://developer.katanamrp.com/reference/updatesupplier) |
| [Update Variant](actions/update-variant.md) | `PATCH /variants/:id` | [docs](https://developer.katanamrp.com/reference/updatevariant) |
