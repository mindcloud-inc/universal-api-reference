# SOS Inventory: Native API Reference

A consolidated summary of SOS Inventory's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developer.sosinventory.com/apidoc/
- **API base URL:** `https://api.sosinventory.com`

## Authentication

### OAuth2

Connect SOS Inventory with OAuth2 authorization code.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.sosinventory.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.sosinventory.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.sosinventory.com/oauth2/token.

[Official authentication documentation](https://developer.sosinventory.com/apidoc/Authentication)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `data`.

## Pagination

Use `maxresults` in the query string to set the page size (default 200; accepted range 1–200). Use `start` in the query string as the record offset; numbering starts at 0.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /api/v2/customer` | [docs](https://developer.sosinventory.com/apidoc/Customer) |
| [Create Estimate](actions/create-estimate.md) | `POST /api/v2/estimate` | [docs](https://developer.sosinventory.com/apidoc/Estimate) |
| [Create Invoice](actions/create-invoice.md) | `POST /api/v2/invoice` | [docs](https://developer.sosinventory.com/apidoc/Invoice) |
| [Create Item](actions/create-item.md) | `POST /api/v2/item` | [docs](https://developer.sosinventory.com/apidoc/Item) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /api/v2/purchaseorder` | [docs](https://developer.sosinventory.com/apidoc/PurchaseOrder) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /api/v2/salesorder` | [docs](https://developer.sosinventory.com/apidoc/SalesOrder) |
| [Create Shipment](actions/create-shipment.md) | `POST /api/v2/shipment` | [docs](https://developer.sosinventory.com/apidoc/Shipment) |
| [Create Transfer](actions/create-transfer.md) | `POST /api/v2/transfer` | [docs](https://developer.sosinventory.com/apidoc/Transfer) |
| [Create Vendor](actions/create-vendor.md) | `POST /api/v2/vendor` | [docs](https://developer.sosinventory.com/apidoc/Vendor) |
| [Get Customer](actions/get-customer.md) | `GET /api/v2/customer/:id` | [docs](https://developer.sosinventory.com/apidoc/Customer) |
| [Get Estimate](actions/get-estimate.md) | `GET /api/v2/estimate/:id` | [docs](https://developer.sosinventory.com/apidoc/Estimate) |
| [Get Invoice](actions/get-invoice.md) | `GET /api/v2/invoice/:id` | [docs](https://developer.sosinventory.com/apidoc/Invoice) |
| [Get Item](actions/get-item.md) | `GET /api/v2/item/:id` | [docs](https://developer.sosinventory.com/apidoc/Item) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /api/v2/purchaseorder/:id` | [docs](https://developer.sosinventory.com/apidoc/PurchaseOrder) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /api/v2/salesorder/:id` | [docs](https://developer.sosinventory.com/apidoc/SalesOrder) |
| [Get Shipment](actions/get-shipment.md) | `GET /api/v2/shipment/:id` | [docs](https://developer.sosinventory.com/apidoc/Shipment) |
| [Get Transfer](actions/get-transfer.md) | `GET /api/v2/transfer/:id` | [docs](https://developer.sosinventory.com/apidoc/Transfer) |
| [Get Vendor](actions/get-vendor.md) | `GET /api/v2/vendor/:id` | [docs](https://developer.sosinventory.com/apidoc/Vendor) |
| [List Customers](actions/list-customers.md) | `GET /api/v2/customer` | [docs](https://developer.sosinventory.com/apidoc/Customer) |
| [List Estimates](actions/list-estimates.md) | `GET /api/v2/estimate` | [docs](https://developer.sosinventory.com/apidoc/Estimate) |
| [List Invoices](actions/list-invoices.md) | `GET /api/v2/invoice` | [docs](https://developer.sosinventory.com/apidoc/Invoice) |
| [List Item Receipts](actions/list-item-receipts.md) | `GET /api/v2/itemreceipt` | [docs](https://developer.sosinventory.com/apidoc/ItemReceipt) |
| [List Items](actions/list-items.md) | `GET /api/v2/item` | [docs](https://developer.sosinventory.com/apidoc/Item) |
| [List Locations](actions/list-locations.md) | `GET /api/v2/location` | [docs](https://developer.sosinventory.com/apidoc/Configuration) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /api/v2/purchaseorder` | [docs](https://developer.sosinventory.com/apidoc/PurchaseOrder) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /api/v2/salesorder` | [docs](https://developer.sosinventory.com/apidoc/SalesOrder) |
| [List Shipments](actions/list-shipments.md) | `GET /api/v2/shipment` | [docs](https://developer.sosinventory.com/apidoc/Customer) |
| [List Transfers](actions/list-transfers.md) | `GET /api/v2/transfer` | [docs](https://developer.sosinventory.com/apidoc/Transfer) |
| [List Vendors](actions/list-vendors.md) | `GET /api/v2/vendor` | [docs](https://developer.sosinventory.com/apidoc/Vendor) |
| [Update Customer](actions/update-customer.md) | `PUT /api/v2/customer/:id` | [docs](https://developer.sosinventory.com/apidoc/Customer) |
| [Update Estimate](actions/update-estimate.md) | `PUT /api/v2/estimate/:id` | [docs](https://developer.sosinventory.com/apidoc/Estimate) |
| [Update Invoice](actions/update-invoice.md) | `PUT /api/v2/invoice/:id` | [docs](https://developer.sosinventory.com/apidoc/Invoice) |
| [Update Item](actions/update-item.md) | `PUT /api/v2/item/:id` | [docs](https://developer.sosinventory.com/apidoc/Item) |
| [Update Purchase Order](actions/update-purchase-order.md) | `PUT /api/v2/purchaseorder/:id` | [docs](https://developer.sosinventory.com/apidoc/PurchaseOrder) |
| [Update Sales Order](actions/update-sales-order.md) | `PUT /api/v2/salesorder/:id` | [docs](https://developer.sosinventory.com/apidoc/SalesOrder) |
| [Update Shipment](actions/update-shipment.md) | `PUT /api/v2/shipment/:id` | [docs](https://developer.sosinventory.com/apidoc/Shipment) |
| [Update Transfer](actions/update-transfer.md) | `PUT /api/v2/transfer/:id` | [docs](https://developer.sosinventory.com/apidoc/Transfer) |
| [Update Vendor](actions/update-vendor.md) | `PUT /api/v2/vendor/:id` | [docs](https://developer.sosinventory.com/apidoc/Vendor) |
