# Amazon Vendor: Native API Reference

A consolidated summary of Amazon Vendor's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://developer-docs.amazon.com/sp-api/reference/welcome-to-api-references
- **API base URL:** `https://sellingpartnerapi-{region}.amazon.com`

## Authentication

### OAuth 2.0

### Credentials

- **Region:** `region` · required · Amazon SP-API region used in the Selling Partner API host.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://vendorcentral.amazon.com/apps/authorize/consent to approve access.
2. Exchange the returned authorization code with a POST request to https://api.amazon.com/auth/o2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


Refresh expired access tokens with a POST request to https://api.amazon.com/auth/o2/token.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `nextToken` in the query string as the pagination cursor.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Direct Fulfillment Shipping Labels](actions/create-direct-fulfillment-shipping-labels.md) | `POST /vendor/directFulfillment/shipping/2021-12-28/shippingLabels/:purchaseOrderNumber` | [docs](https://developer-docs.amazon.com/sp-api/reference/createshippinglabels) |
| [Get Direct Fulfillment Packing Slip](actions/get-direct-fulfillment-packing-slip.md) | `GET /vendor/directFulfillment/shipping/2021-12-28/packingSlips/:purchaseOrderNumber` | [docs](https://developer-docs.amazon.com/sp-api/reference/getpackingslip-1) |
| [Get Direct Fulfillment Shipping Label](actions/get-direct-fulfillment-shipping-label.md) | `GET /vendor/directFulfillment/shipping/2021-12-28/shippingLabels/:purchaseOrderNumber` | [docs](https://developer-docs.amazon.com/sp-api/reference/getshippinglabel-1) |
| [Get Direct Fulfillment Transaction Status](actions/get-direct-fulfillment-transaction-status.md) | `GET /vendor/directFulfillment/transactions/2021-12-28/transactions/:transactionId` | [docs](https://developer-docs.amazon.com/sp-api/reference/gettransactionstatus-1) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /vendor/orders/v1/purchaseOrders/:purchaseOrderNumber` | [docs](https://developer-docs.amazon.com/sp-api/reference/getpurchaseorder) |
| [Get Purchase Orders](actions/get-purchase-orders.md) | `GET /vendor/orders/v1/purchaseOrders` | [docs](https://developer-docs.amazon.com/sp-api/reference/getpurchaseorders) |
| [List Direct Fulfillment Orders](actions/list-direct-fulfillment-orders.md) | `GET /vendor/directFulfillment/orders/2021-12-28/purchaseOrders` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorders-2) |
| [Submit Direct Fulfillment Acknowledgements](actions/submit-direct-fulfillment-acknowledgements.md) | `POST /vendor/directFulfillment/orders/2021-12-28/acknowledgements` | [docs](https://developer-docs.amazon.com/sp-api/reference/submitacknowledgement-2) |
| [Submit Direct Fulfillment Invoices](actions/submit-direct-fulfillment-invoices.md) | `POST /vendor/directFulfillment/payments/v1/invoices` | [docs](https://developer-docs.amazon.com/sp-api/reference/submitinvoice) |
| [Submit Direct Fulfillment Shipment Confirmations](actions/submit-direct-fulfillment-shipment-confirmations.md) | `POST /vendor/directFulfillment/shipping/v1/shipmentConfirmations` | [docs](https://developer-docs.amazon.com/sp-api/reference/submitshipmentconfirmations-1) |
| [Submit Purchase Order Acknowledgements](actions/submit-purchase-order-acknowledgements.md) | `POST /vendor/orders/v1/acknowledgements` | [docs](https://developer-docs.amazon.com/sp-api/reference/submitacknowledgement) |
| [Submit Shipment Confirmations](actions/submit-shipment-confirmations.md) | `POST /vendor/shipping/v1/shipmentConfirmations` | [docs](https://developer-docs.amazon.com/sp-api/reference/submitshipmentconfirmations) |
