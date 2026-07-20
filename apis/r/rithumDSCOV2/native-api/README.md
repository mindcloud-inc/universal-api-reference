# Rithum DSCO: Native API Reference

A consolidated summary of Rithum DSCO's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://api.dsco.io/doc/v3/reference/
- **OpenAPI specification:** https://api.dsco.io/doc/v3/dsco-api-spec.yaml
- **API base URL:** `https://api.dsco.io/api/v3`

## Authentication

### OAuth2 Client Credentials

Use Rithum DSCO OAuth2 client credentials to mint bearer tokens for the DSCO v3 API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.dsco.io/api/v3/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://api.dsco.io/doc/v3/reference/#tag/OAuth2/operation/getAccessToken)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Order Items](actions/acknowledge-order-items.md) | `POST order/acknowledge/items` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/acknowledgeOrderItems) |
| [Acknowledge Orders](actions/acknowledge-orders.md) | `POST order/acknowledge` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/acknowledgeOrders) |
| [Cancel Order Item](actions/cancel-order-item.md) | `POST order/item/cancel` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/cancelOrderItem) |
| [Create Assortment](actions/create-assortment.md) | `POST assortment` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Assortment/operation/createAssortment) |
| [Create Order](actions/create-order.md) | `POST order` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/createOrder) |
| [Delete Assortment](actions/delete-assortment.md) | `DELETE assortment/:id` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Assortment/operation/deleteAssortment) |
| [Get Assortment](actions/get-assortment.md) | `GET assortment/:id` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Assortment/operation/getAssortment) |
| [List Assortments](actions/get-assortments.md) | `GET assortment` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Assortment/operation/getAssortments) |
| [Get Catalog Object](actions/get-catalog-by-id.md) | `GET catalog` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Catalog/operation/getCatalogById) |
| [Get Catalog Change Log](actions/get-catalog-change-log.md) | `GET catalog/log` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Catalog/operation/getCatalogChangeLog) |
| [Get Inventory Object](actions/get-inventory-by-id.md) | `GET inventory` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Inventory/operation/getInventoryById) |
| [Get Invoice](actions/get-invoice-by-id.md) | `GET invoice` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Invoice/operation/getInvoiceById) |
| [Get Order](actions/get-order-by-id.md) | `GET order` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/getOrderById) |
| [Get Order Change Log](actions/get-order-change-log.md) | `GET order/log` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/getOrderChangeLog) |
| [Get Warehouses](actions/get-warehouses.md) | `GET warehouse/page` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Warehouse/operation/getWarehouses) |
| [List Orders](actions/list-orders.md) | `GET order/page` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/getOrders) |
| [Create Invoice](actions/single-invoice.md) | `POST invoice` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Invoice/operation/singleInvoice) |
| [Update Single Inventory](actions/single-item.md) | `POST inventory/singleItem` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Inventory/operation/singleItem) |
| [Create Shipment](actions/single-shipment.md) | `POST order/singleShipment` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/singleShipment) |
| [Test Connection](actions/test-connection.md) | `GET hello` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Hello/operation/helloWorld) |
| [Update Assortment](actions/update-assortment.md) | `PUT assortment/:id` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Assortment/operation/updateAssortment) |
| [Update Catalog Small Batch](actions/update-catalog-small-batch.md) | `POST catalog/batch/small` | [docs](https://api.dsco.io/doc/v3/reference/#tag/Catalog/operation/updateCatalogSmallBatch) |
