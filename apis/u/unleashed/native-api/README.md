# Unleashed: Native API Reference

A consolidated summary of Unleashed's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.unleashedsoftware.com
- **API base URL:** `https://api.unleashedsoftware.com`

## Authentication

### Signed API Headers

Connect using your Unleashed API Id and Private Key.

### Credentials

- **API Id:** `apiAuthId` · required · Paste the API Id from Unleashed API Access.
- **API Key:** `apiKey` · required · Paste the Private Key from Unleashed API Access.

[Official authentication documentation](https://apidocs.unleashedsoftware.com/AuthenticationHelp)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`. The total page count is read from `pagination.numberOfPages`. The current page number is read from `pagination.pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size (default 200; accepted range 1–1000). Use `pageNumber` in the request parameters to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `sort`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /Customers` | [docs](https://apidocs.unleashedsoftware.com/Customers) |
| [Create Product](actions/create-product.md) | `POST /Products` | [docs](https://apidocs.unleashedsoftware.com/Products) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /PurchaseOrders` | [docs](https://apidocs.unleashedsoftware.com/Purchases) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /SalesOrders` | [docs](https://apidocs.unleashedsoftware.com/SalesOrders) |
| [Create Sales Shipment](actions/create-sales-shipment.md) | `POST /SalesShipments` | [docs](https://apidocs.unleashedsoftware.com/SalesShipments) |
| [Delete Purchase Order](actions/delete-purchase-order.md) | `DELETE /PurchaseOrders/:orderGuid` | [docs](https://apidocs.unleashedsoftware.com/Purchases) |
| [Delete Sales Order](actions/delete-sales-order.md) | `DELETE /SalesOrders/:orderGuid` | [docs](https://apidocs.unleashedsoftware.com/SalesOrders) |
| [Delete Sales Shipment](actions/delete-sales-shipment.md) | `DELETE /SalesShipments/:salesShipmentGuid` | [docs](https://apidocs.unleashedsoftware.com/SalesShipments) |
| [Get Customer](actions/get-customer.md) | `GET /Customers/:customerGuid` | [docs](https://apidocs.unleashedsoftware.com/Customers) |
| [Get Product](actions/get-product.md) | `GET /Products/:productGuid` | [docs](https://apidocs.unleashedsoftware.com/Products) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /PurchaseOrders/:orderGuid` | [docs](https://apidocs.unleashedsoftware.com/Purchases) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /SalesOrders/:orderGuid` | [docs](https://apidocs.unleashedsoftware.com/SalesOrders) |
| [Get Sales Shipment](actions/get-sales-shipment.md) | `GET /SalesShipments/:salesShipmentGuid` | [docs](https://apidocs.unleashedsoftware.com/SalesShipments) |
| [List Customer Contacts](actions/list-customer-contacts.md) | `GET /Customers/:customerGuid/Contacts` | [docs](https://apidocs.unleashedsoftware.com/Customers) |
| [List Customers](actions/list-customers.md) | `GET /Customers/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/Customers) |
| [List Products](actions/list-products.md) | `GET /Products/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/Products) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /PurchaseOrders/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/Purchases) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /SalesOrders/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/SalesOrders) |
| [List Sales Shipments](actions/list-sales-shipments.md) | `GET /SalesShipments/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/SalesShipments) |
| [List Stock On Hand](actions/list-stock-on-hand.md) | `GET /StockOnHand/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/StockOnHand) |
| [List Suppliers](actions/list-suppliers.md) | `GET /Suppliers/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/Suppliers) |
| [List Warehouses](actions/list-warehouses.md) | `GET /Warehouses/:pageNumber` | [docs](https://apidocs.unleashedsoftware.com/Warehouses) |
| [Update Customer](actions/update-customer.md) | `POST /Customers/:customerGuid` | [docs](https://apidocs.unleashedsoftware.com/Customers) |
| [Update Product](actions/update-product.md) | `POST /Products/:productGuid` | [docs](https://apidocs.unleashedsoftware.com/Products) |
| [Update Purchase Order](actions/update-purchase-order.md) | `PUT /PurchaseOrders/:orderGuid` | [docs](https://apidocs.unleashedsoftware.com/Purchases) |
| [Update Sales Order](actions/update-sales-order.md) | `PUT /SalesOrders/:orderGuid` | [docs](https://apidocs.unleashedsoftware.com/SalesOrders) |
| [Update Sales Shipment](actions/update-sales-shipment.md) | `PUT /SalesShipments/:salesShipmentGuid` | [docs](https://apidocs.unleashedsoftware.com/SalesShipments) |
