# BaseLinker: Native API Reference

A consolidated summary of BaseLinker's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.baselinker.com/
- **API base URL:** `https://api.baselinker.com`

## Authentication

### API Key

Connect with a BaseLinker API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.baselinker.com/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded; charset=UTF-8` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Order Product](actions/add-order-product.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=addOrderProduct) |
| [Create Package](actions/create-package.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=createPackage) |
| [Delete Order Product](actions/delete-order-product.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=deleteOrderProduct) |
| [Get Courier Accounts](actions/get-courier-accounts.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getCourierAccounts) |
| [Get Couriers List](actions/get-couriers-list.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getCouriersList) |
| [Get Inventories](actions/get-inventories.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getInventories) |
| [Get Inventory Products Data](actions/get-inventory-products-data.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getInventoryProductsData) |
| [Get Inventory Products List](actions/get-inventory-products-list.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getInventoryProductsList) |
| [Get Inventory Products Prices](actions/get-inventory-products-prices.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getInventoryProductsPrices) |
| [Get Inventory Products Stock](actions/get-inventory-products-stock.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getInventoryProductsStock) |
| [Get Inventory Warehouses](actions/get-inventory-warehouses.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getInventoryWarehouses) |
| [Get Order Packages](actions/get-order-packages.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getOrderPackages) |
| [Get Order Payments History](actions/get-order-payments-history.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getOrderPaymentsHistory) |
| [Get Order Sources](actions/get-order-sources.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getOrderSources) |
| [Get Order Statuses](actions/get-order-statuses.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getOrderStatusList) |
| [Get Orders](actions/get-orders.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getOrders) |
| [Get Orders by Email](actions/get-orders-by-email.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=getOrdersByEmail) |
| [Set Order Fields](actions/set-order-fields.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=setOrderFields) |
| [Set Order Payment](actions/set-order-payment.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=setOrderPayment) |
| [Set Order Product Fields](actions/set-order-product-fields.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=setOrderProductFields) |
| [Set Order Status](actions/set-order-status.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=setOrderStatus) |
| [Set Order Statuses](actions/set-order-statuses.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=setOrderStatuses) |
| [Update Inventory Products Prices](actions/update-inventory-products-prices.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=updateInventoryProductsPrices) |
| [Update Inventory Products Stock](actions/update-inventory-products-stock.md) | `POST /connector.php` | [docs](https://api.baselinker.com/index.php?method=updateInventoryProductsStock) |
