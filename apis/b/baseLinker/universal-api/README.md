# <img src="https://images.mindcloud.co/apps/icons/base-linker_1773750535732.png" alt="BaseLinker logo" width="28" height="28"> BaseLinker: Universal API

Manage orders, inventory, shipments, and ecommerce operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/baseLinker/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://base.com/
- **Vendor API docs:** https://api.baselinker.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Order Sources](actions/get-order-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventories](actions/get-inventories.md) | GET | Retrieves inventories from BaseLinker. |

### Order Product

| Action | Method | Description |
| --- | --- | --- |
| [Add Order Product](actions/add-order-product.md) | POST | Adds a product to an order in BaseLinker. |
| [Delete Order Product](actions/delete-order-product.md) | DELETE | Deletes a product from an order in BaseLinker. |
| [Set Order Product Fields](actions/set-order-product-fields.md) | PUT | Updates order product fields in BaseLinker. |

### Order Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Sources](actions/get-order-sources.md) | GET | Retrieves order sources from BaseLinker. |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Statuses](actions/get-order-statuses.md) | GET | Retrieves order statuses from BaseLinker. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Orders](actions/get-orders.md) | GET | Retrieves orders from BaseLinker. |
| [Get Orders by Email](actions/get-orders-by-email.md) | GET | Finds orders in BaseLinker by email address. |
| [Set Order Fields](actions/set-order-fields.md) | PUT | Updates order fields in BaseLinker. |
| [Set Order Status](actions/set-order-status.md) | PUT | Updates an order status in BaseLinker. |
| [Set Order Statuses](actions/set-order-statuses.md) | PUT | Updates multiple order statuses in BaseLinker. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Payments History](actions/get-order-payments-history.md) | GET | Retrieves payment history for an order in BaseLinker. |
| [Set Order Payment](actions/set-order-payment.md) | PUT | Updates order payment details in BaseLinker. |

### Product Stock

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Products Stock](actions/get-inventory-products-stock.md) | GET | Retrieves inventory product stock from BaseLinker. |
| [Update Inventory Products Stock](actions/update-inventory-products-stock.md) | PUT | Updates inventory product stock in BaseLinker. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Products Data](actions/get-inventory-products-data.md) | GET | Retrieves inventory product details from BaseLinker. |
| [Get Inventory Products List](actions/get-inventory-products-list.md) | GET | Retrieves basic inventory product data from BaseLinker. |
| [Get Inventory Products Prices](actions/get-inventory-products-prices.md) | GET | Retrieves inventory product prices from BaseLinker. |
| [Update Inventory Products Prices](actions/update-inventory-products-prices.md) | PUT | Updates inventory product prices in BaseLinker. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Create Package](actions/create-package.md) | POST | Creates a shipping package in BaseLinker. |
| [Get Courier Accounts](actions/get-courier-accounts.md) | GET | Retrieves courier accounts from BaseLinker. |
| [Get Couriers List](actions/get-couriers-list.md) | GET | Retrieves couriers from BaseLinker. |
| [Get Order Packages](actions/get-order-packages.md) | GET | Retrieves packages for an order from BaseLinker. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Warehouses](actions/get-inventory-warehouses.md) | GET | Retrieves inventory warehouses from BaseLinker. |

