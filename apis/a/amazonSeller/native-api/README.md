# Amazon Seller: Native API Reference

A consolidated summary of Amazon Seller's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developer-docs.amazon.com/sp-api/reference/welcome-to-api-references
- **REST base URL:** `https://{environment}-{region}.amazon.com`
- **PageSize / PageStartIndex base URL:** `https://{environment}-{region}.amazon.com`
- **pageSize / paginationToken base URL:** `https://{environment}-{region}.amazon.com`
- **QueryType / NextToken base URL:** `https://{environment}-{region}.amazon.com`
- **pageSize / nextToken base URL:** `https://{environment}-{region}.amazon.com`
- **pageSize / pageToken base URL:** `https://{environment}-{region}.amazon.com`
- **nextToken base URL:** `https://{environment}-{region}.amazon.com`

## Authentication

### OAuth 2.0

### Credentials

- **Region:** `region` · required
- **Marketplace:** `marketplace` · required
- **Environment:** `environment` · required
- **Seller ID:** `sellerID` · optional

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.marketplace}}/apps/authorize/consent to approve access.
2. Exchange the returned authorization code with a POST request to https://api.amazon.com/auth/o2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


Refresh expired access tokens with a POST request to https://api.amazon.com/auth/o2/token.

[Official authentication documentation](https://developer-docs.amazon.com/sp-api/docs/website-authorization-workflow)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

### PageSize / PageStartIndex

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### pageSize / paginationToken

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### QueryType / NextToken

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

### pageSize / nextToken

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `feeds`.

### pageSize / pageToken

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `pagination.nextToken`.

### nextToken

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

- **REST:** Use `maxResultsPerPage` in the query string to set the page size (default 50; accepted range 1–100). Use `paginationToken` in the query string as the pagination cursor.
- **PageSize / PageStartIndex:** Use `PageSize` in the query string to set the page size (default 250; maximum 1000). Use `PageStartIndex` in the query string to choose the page; numbering starts at 0.
- **pageSize / paginationToken:** Use `pageSize` in the query string to set the page size (default 10; accepted range 1–30). Use `paginationToken` in the query string as the pagination cursor.
- **QueryType / NextToken:** Use `NextToken` in the query string as the pagination cursor.
- **pageSize / nextToken:** Use `pageSize` in the query string to set the page size (default 10; accepted range 1–100). Use `nextToken` in the query string as the pagination cursor.
- **pageSize / pageToken:** Use `pageSize` in the query string to set the page size (default 10; maximum 20). Use `pageToken` in the query string as the pagination cursor.
- **nextToken:** Use `limit` in the query string to set the page size (maximum 50). Use `nextToken` in the query string as the pagination cursor.

## Sorting

- **pageSize / pageToken:** Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

- **REST:** Stop after 3 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (37 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Cancel Shipment](actions/cancel-shipment.md) | REST | `DELETE mfn/v0/shipments/:shipmentId` | [docs](https://developer-docs.amazon.com/sp-api/reference/cancelshipment) |
| [Confirm Shipment](actions/confirm-shipment.md) | REST | `POST orders/v0/orders/:orderId/shipmentConfirmation` | [docs](https://developer-docs.amazon.com/sp-api/reference/confirmshipment) |
| [Create FBM Listings Inventory Report](actions/create-fbm-listings-inventory-report.md) | REST | `POST reports/2021-06-30/reports` | [docs](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#createreport) |
| [Create Fulfillment Order](actions/create-fulfillment-order.md) | REST | `POST https://sellingpartnerapi-na.amazon.com/fba/outbound/2020-07-01/fulfillmentOrders` | [docs](https://developer-docs.amazon.com/sp-api/reference/confirmshipment) |
| [Create Shipment](actions/create-shipment.md) | REST | `POST mfn/v0/shipments` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorders) |
| [Get Account](actions/get-account.md) | REST | `GET sellers/v1/account` | [docs](https://developer-docs.amazon.com/sp-api/reference/getaccount) |
| [Get Bill of Lading](actions/get-bill-of-lading.md) | REST | `GET fba/inbound/v0/shipments/:shipmentId/billOfLading` | [docs](https://developer-docs.amazon.com/sp-api/reference/getbilloflading) |
| [Get Eligible Shipment Services](actions/get-eligible-shipment-services.md) | REST | `POST mfn/v0/eligibleShippingServices` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorders) |
| [Get FBM Report Document](actions/get-fbm-report-document.md) | REST | `GET reports/2021-06-30/documents/:reportDocumentId` | [docs](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#getreportdocument) |
| [Get FBM Report Status](actions/get-fbm-report-status.md) | REST | `GET reports/2021-06-30/reports/:reportId` | [docs](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#getreport) |
| [Get Fulfillment Preview](actions/get-fulfillment-preview.md) | REST | `POST https://sellingpartnerapi-na.amazon.com/fba/outbound/2020-07-01/fulfillmentOrders/preview` | [docs](https://developer-docs.amazon.com/sp-api/reference/confirmshipment) |
| [Get Inbound Plan](actions/get-inbound-plan.md) | REST | `GET inbound/fba/2024-03-20/inboundPlans/:inboundPlanId` | [docs](https://developer-docs.amazon.com/sp-api/reference/getinboundplan) |
| [Get FBA Inventory Summaries (AFN only)](actions/get-inventory-summaries.md) | REST | `GET fba/inventory/v1/summaries` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorders) |
| [Get Labels](actions/get-labels.md) | PageSize / PageStartIndex | `GET fba/inbound/v0/shipments/:shipmentId/label` | [docs](https://developer-docs.amazon.com/sp-api/reference/getlabels) |
| [Get Listings Item](actions/get-listings-item.md) | REST | `GET listings/2021-08-01/items/{{credentials.sellerID}}/:sku` | [docs](https://developer-docs.amazon.com/sp-api/reference/getlistingsitem) |
| [Get Marketplace Participations](actions/get-marketplace-participations.md) | REST | `GET sellers/v1/marketplaceParticipations` | [docs](https://developer-docs.amazon.com/sp-api/reference/getmarketplaceparticipations) |
| [Get Order Address](actions/get-order-address.md) | REST | `GET orders/v0/orders/:orderId/address` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorderaddress) |
| [Get Order Buyer Info](actions/get-order-buyer-info.md) | REST | `GET orders/v0/orders/:orderId/buyerInfo` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorderbuyerinfo) |
| [Get Order Metrics](actions/get-order-metrics.md) | REST | `GET sales/v1/orderMetrics` | [docs](https://developer-docs.amazon.com/sp-api/reference/getordermetrics) |
| [Get Order Regulated Info](actions/get-order-regulated-info.md) | REST | `GET orders/v0/orders/:orderId/regulatedInfo` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorderregulatedinfo) |
| [Get Order](actions/get-order-v2026.md) | REST | `GET orders/2026-01-01/orders/:orderId` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorder-3) |
| [List Shipment Items](actions/get-shipment-items.md) | QueryType / NextToken | `GET fba/inbound/v0/shipmentItems` | [docs](https://developer-docs.amazon.com/sp-api/reference/getshipmentitems) |
| [Get Shipment Items by ID](actions/get-shipment-items-by-id.md) | QueryType / NextToken | `GET fba/inbound/v0/shipments/:shipmentId/items` | [docs](https://developer-docs.amazon.com/sp-api/reference/getorders) |
| [Get Shipment ( MFN )](actions/get-shipment-mfn.md) | REST | `GET mfn/v0/shipments/:shipmentId` | [docs](https://developer-docs.amazon.com/sp-api/reference/getshipments) |
| [List Financial Events by Order ID](actions/list-financial-events-by-order-id.md) | REST | `GET finances/v0/orders/:orderId/financialEvents` | [docs](https://developer-docs.amazon.com/sp-api/reference/listfinancialeventsbyorderid) |
| [List Inbound Plans](actions/list-inbound-plans.md) | pageSize / paginationToken | `GET inbound/fba/2024-03-20/inboundPlans` | [docs](https://developer-docs.amazon.com/sp-api/reference/listinboundplans) |
| [List Shipments](actions/list-inbound-shipments.md) | QueryType / NextToken | `GET fba/inbound/v0/shipments` | [docs](https://developer-docs.amazon.com/sp-api/reference/getshipments) |
| [List Settlement Report List](actions/list-settlement-report-list.md) | REST | `GET reports/2021-06-30/reports` | [docs](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#getreports) |
| [List Transactions](actions/list-transactions.md) | REST | `GET finances/2024-06-19/transactions` | [docs](https://developer-docs.amazon.com/sp-api/reference/listtransactions) |
| [Patch Listings Item](actions/patch-listings-item.md) | REST | `PATCH listings/2021-08-01/items/:sellerId/:sku` | [docs](https://developer-docs.amazon.com/sp-api/reference/patchlistingsitem) |
| [Search Catalog Items by Identifier](actions/search-catalog-items-by-identifier.md) | REST | `GET catalog/2022-04-01/items` | [docs](https://developer-docs.amazon.com/sp-api/reference/searchcatalogitems) |
| [Search Listings Items](actions/search-listings-items.md) | pageSize / pageToken | `GET listings/2021-08-01/items/{{credentials.sellerID}}` | [docs](https://developer-docs.amazon.com/sp-api/reference/searchlistingsitems) |
| [Search Orders](actions/search-orders-v2026.md) | REST | `GET orders/2026-01-01/orders` | [docs](https://developer-docs.amazon.com/sp-api/reference/searchorders) |
| [Update LTL Shipment Tracking Details](actions/update-ltl-shipment-tracking-details.md) | REST | `POST inbound/fba/2024-03-20/inboundPlans/:inboundPlanId/shipments/:shipmentId/trackingDetails` | [docs](https://developer-docs.amazon.com/sp-api/reference/updateshipmenttrackingdetails) |
| [Update Shipment Status](actions/update-shipment-status.md) | REST | `POST orders/v0/orders/:orderId/shipment` | [docs](https://developer-docs.amazon.com/sp-api/reference/updateshipmentstatus) |
| [Update SPD Shipment Tracking Details](actions/update-spd-shipment-tracking-details.md) | REST | `POST inbound/fba/2024-03-20/inboundPlans/:inboundPlanId/shipments/:shipmentId/trackingDetails` | [docs](https://developer-docs.amazon.com/sp-api/reference/updateshipmenttrackingdetails) |
| [Update Verification Status](actions/update-verification-status.md) | REST | `PATCH orders/v0/orders/:orderId/regulatedInfo` | [docs](https://developer-docs.amazon.com/sp-api/reference/updateverificationstatus) |
