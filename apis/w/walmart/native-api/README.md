# Walmart: Native API Reference

A consolidated summary of Walmart's API configuration and 90 documented operations, with links to official documentation.

- **Official docs:** https://developer.walmart.com/us-marketplace/reference
- **REST base URL:** `https://{environment}.walmartapis.com`
- **Simulations base URL:** `https://sandbox.walmartapis.com`
- **REST (nextCursor) base URL:** `https://{environment}.walmartapis.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.account.wal-mart.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://marketplace.walmartapis.com/v3/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


Refresh expired access tokens with a POST request to https://marketplace.walmartapis.com/v3/token.

[Official authentication documentation](https://developer.walmart.com/us-marketplace/docs/find-and-connect-a-solution-provider)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### Simulations

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST (nextCursor)

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

- **REST:** Use `noOfRecords` in the query string to set the page size (default 100; maximum 200). Use `offset` in the query string as the record offset.
- **REST (nextCursor):** Use `limit` in the query string to set the page size (default 20; maximum 1000). Use `offset` in the query string as the record offset.

## Filtering

- **REST:** Supported operators: `eq`.

## Endpoints (90 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Acknowledge Orders](actions/acknowledge-orders.md) | REST | `POST /v3/orders/:purchaseOrderId/acknowledge` | [docs](https://developer.walmart.com/us-marketplace/reference/acknowledgeorders) |
| [Available Recon Report Dates](actions/available-recon-report-dates.md) | REST | `GET /v3/report/reconreport/availableReconFiles?reportVersion=v1` | [docs](https://developer.walmart.com/global-marketplace/reference/getallorders) |
| [Bulk Item Enrollment for Walmart+](actions/bulk-item-enrollment-for-walmart-plus.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/post_v3-feeds) |
| [Bulk Item Inventory Update](actions/bulk-item-inventory-update.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/post_v3-feeds) |
| [Bulk Item Setup - Delete Items](actions/bulk-item-setup-delete-items.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/itembulkuploads#:~:text=Utilities-,Bulk%20Item%20Setup%20%28Multiple%29,-POST) |
| [Bulk Item Setup (multiple)](actions/bulk-item-setup-multiple.md) | REST | `POST v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/itembulkuploads) |
| [Bulk Item Setup - Retire Items](actions/bulk-item-setup-retire-items.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/itembulkuploads#:~:text=Utilities-,Bulk%20Item%20Setup%20%28Multiple%29,-POST) |
| [Bulk Item Setup - Seller Fulfilled](actions/bulk-item-setup-seller-fulfilled.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/itembulkuploads) |
| [Bulk Item Setup - WFS](actions/bulk-item-setup-wfs.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/itembulkuploads) |
| [Bulk Update Price ( Legacy )](actions/bulk-update-price-legacy.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/pricebulkuploads#:~:text=Utilities-,Update%20Bulk%20Prices%20%28Multiple%29,-POST) |
| [Bulk Update Price ( New )](actions/bulk-update-price-new.md) | REST | `POST v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/pricebulkuploads-1) |
| [Bulk Update Promotional Price](actions/bulk-update-promotional-price.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/global-marketplace/reference/pricebulkuploads) |
| [Cancel Inbound Shipment](actions/cancel-inbound-shipment.md) | REST | `DELETE /v3/fulfillment/inbound-shipments/:inboundOrderId` | [docs](https://developer.walmart.com/global-marketplace/reference/cancelshipment) |
| [Cancel Order Lines](actions/cancel-order-lines.md) | REST | `POST /v3/orders/:purchaseOrderId/cancel` | [docs](https://developer.walmart.com/us-marketplace/reference/acknowledgeorders) |
| [Check Eligibility of Items](actions/check-eligibility-of-items.md) | REST | `POST v3/advertising/sem/items/eligibility` | [docs](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails) |
| [Create Campaign](actions/create-campaign.md) | REST | `POST v3/advertising/sem/campaigns` | [docs](https://developer.walmart.com/us-marketplace/reference/createcampaign) |
| [Create Subscription](actions/create-subscription.md) | REST | `POST /v3/webhooks/subscriptions` | [docs](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions) |
| [Create 3rd Party Fulfillment Center Association](actions/create3rd-party-fulfillment-center-association.md) | REST | `POST /v3/settings/shipping/3plshipnodes` | [docs](https://developer.walmart.com/us-marketplace/reference/associate3pfulfillmentcenter) |
| [Delete Campaign](actions/delete-campaign.md) | REST | `DELETE v3/advertising/sem/campaigns/:campaignId` | [docs](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails) |
| [Delete Shipping Template](actions/delete-shipping-template.md) | REST | `DELETE /v3/settings/shipping/templates/:templateId` | [docs](https://developer.walmart.com/us-marketplace/reference/deleteshippingtemplatedetails) |
| [Delete Subscription](actions/delete-subscription.md) | REST | `DELETE v3/webhooks/subscriptions/:subscriptionId` | [docs](https://developer.walmart.com/us-marketplace/reference/deletesubscription) |
| [Discard Label](actions/discard-label.md) | REST | `DELETE /v3/shipping/labels/carriers/:carrierShortName/trackings/:trackingNo` | [docs](https://developer.walmart.com/us-marketplace/reference/discardlabel) |
| [Download Label](actions/download-label.md) | REST | `GET /v3/shipping/labels/carriers/:carrierShortName/trackings/:trackingNo` | [docs](https://developer.walmart.com/us-marketplace/reference/getlabelbytrackingandcarrier) |
| [Get Account Settings](actions/get-account-settings.md) | REST | `GET /v3/settings/shipping/account` | [docs](https://developer.walmart.com/us-marketplace/reference/getaccountlevelsettings) |
| [List Orders](actions/get-all-orders.md) | REST | `GET /v3/orders` | [docs](https://developer.walmart.com/global-marketplace/reference/getallorders) |
| [Get Campaign Details](actions/get-campaign-details.md) | REST | `GET v3/advertising/sem/campaigns/:campaignId` | [docs](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails) |
| [Get Event Types](actions/get-event-types.md) | REST | `GET /v3/webhooks/eventTypes` | [docs](https://developer.walmart.com/us-marketplace/reference/geteventtypes) |
| [Get Feed Error Report](actions/get-feed-error-report.md) | REST | `GET /v3/feeds/:feedId/errorReport` | [docs](https://developer.walmart.com/us-marketplace/reference/getallfeedstatuses#:~:text=Utilities-,All%20feed%20statuses,-GET) |
| [Get Feed Item Status](actions/get-feed-item-status.md) | REST | `GET /v3/feeds/:feedId` | [docs](https://developer.walmart.com/us-marketplace/reference/getallfeedstatuses#:~:text=Utilities-,All%20feed%20statuses,-GET) |
| [Get Fulfillment Center Coverages](actions/get-fulfillment-center-coverages.md) | REST | `GET /v3/settings/shipping/shipnodes/coverage` | [docs](https://developer.walmart.com/us-marketplace/reference/getcoverageforfulfillmentcenters) |
| [Get Inbound Shipment Errors](actions/get-inbound-shipment-errors.md) | REST | `GET /v3/fulfillment/inbound-shipment-errors` | [docs](https://developer.walmart.com/us-marketplace/reference/getinboundshipmentitems) |
| [Get Inbound Shipment Items](actions/get-inbound-shipment-items.md) | REST | `GET /v3/fulfillment/inbound-shipment-items` | [docs](https://developer.walmart.com/us-marketplace/reference/getinboundshipmentitems) |
| [Get Inventory](actions/get-inventory.md) | REST | `GET /v3/inventory` | [docs](https://developer.walmart.com/us-marketplace/reference/getallitems) |
| [Get Item](actions/get-item.md) | REST | `GET /v3/items/:id` | [docs](https://developer.walmart.com/us-marketplace/reference/getanitem) |
| [Get Item Associations](actions/get-item-associations.md) | REST | `POST /v3/items/associations` | [docs](https://developer.walmart.com/us-marketplace/reference/getitemassociations) |
| [Get Item Count by Groups](actions/get-item-count-by-groups.md) | REST | `GET /v3/items/groups/count` | [docs](https://developer.walmart.com/us-marketplace/reference/getvariantcount) |
| [Get Item Count by Status](actions/get-item-count-by-status.md) | REST | `GET /v3/items/count` | [docs](https://developer.walmart.com/us-marketplace/reference/getvariantcount) |
| [Get Label Details](actions/get-label-details.md) | REST | `GET /v3/shipping/labels/purchase-orders/:purchaseOrderId` | [docs](https://developer.walmart.com/us-marketplace/reference/getlabel#:~:text=Utilities-,Labels%20detail%20by%20purchase%20order%20id,-GET) |
| [Get Lag Time](actions/get-lag-time.md) | REST | `GET /v3/lagtime` | [docs](https://developer.walmart.com/us-marketplace/reference/getlagtime) |
| [Get Order](actions/get-order.md) | REST | `GET /v3/orders/:purchaseOrderId` | [docs](https://developer.walmart.com/global-marketplace/reference/getallorders) |
| [Get Partner Configurations](actions/get-partner-configurations.md) | REST | `GET /v3/settings/partnerprofile` | [docs](https://developer.walmart.com/us-marketplace/reference/getpartnerconfigurations) |
| [Get Promotional Prices](actions/get-promotional-prices.md) | REST | `GET v3/promo/sku/:sku` | [docs](https://developer.walmart.com/global-marketplace/reference/getpromotionalprices) |
| [Get Shipping Configurations](actions/get-shipping-configurations.md) | REST | `GET /v3/settings/shippingprofile` | [docs](https://developer.walmart.com/us-marketplace/reference/getshippingconfigurations) |
| [Get Shipping Template Activation Status](actions/get-shipping-template-activation-status.md) | REST | `GET /v3/settings/shipping/templates/activationStatus` | [docs](https://developer.walmart.com/us-marketplace/reference/getshippingtemplateactivationstatus) |
| [Get Shipping Template Details](actions/get-shipping-template-details.md) | REST | `GET /v3/settings/shipping/templates/:templateId` | [docs](https://developer.walmart.com/us-marketplace/reference/getshippingtemplatedetails) |
| [Get Simplified Shipping Settings](actions/get-simplified-shipping-settings.md) | REST | `GET /v3/settings/shipping/simplifiedshippingsettings` | [docs](https://developer.walmart.com/us-marketplace/reference/getsimplifiedshippingsettings) |
| [Get Single Item Inventory by Ship Node](actions/get-single-item-inventory-by-ship-node.md) | REST | `GET /v3/inventories/:sku` | [docs](https://developer.walmart.com/us-marketplace/reference/getmultinodeinventoryforskuandallshipnodes) |
| [Get Spec](actions/get-spec.md) | REST | `POST /v3/items/spec` | [docs](https://developer.walmart.com/us-marketplace/reference/getspec) |
| [Get Supported Carrier Package Types](actions/get-supported-carrier-package-types.md) | REST | `GET /v3/shipping/labels/carriers/:carrierShortName/package-types` | [docs](https://developer.walmart.com/us-marketplace/reference/getcarrierpackagetypes) |
| [Get Taxonomy](actions/get-taxonomy.md) | REST | `GET /v3/items/taxonomy` | [docs](https://developer.walmart.com/us-marketplace/reference/gettaxonomyresponse) |
| [Get Taxonomy by Spec](actions/get-taxonomy-by-spec.md) | REST | `GET /v3/utilities/taxonomy` | [docs](https://developer.walmart.com/us-marketplace/reference/gettaxonomyresponse-1) |
| [Get Token Detail](actions/get-token-detail.md) | REST | `GET /v3/token/detail` | [docs](https://developer.walmart.com/us-marketplace/reference/gettokendetail) |
| [Get Top Recommended Catalog Items](actions/get-top-recommended-catalog-items.md) | REST | `GET v3/advertising/sem/items/recommendations` | [docs](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails) |
| [Get Walmart API Status](actions/get-walmart-api-status.md) | REST | `GET v3/utilities/apiStatus` | [docs](https://developer.walmart.com/us-marketplace/reference/getapiplatformstatus) |
| [Get WFS Inventory](actions/get-wfs-inventory.md) | REST | `GET /v3/wfs/inventory` | [docs](https://developer.walmart.com/us-marketplace/reference/getwfsinventorydetails) |
| [Get WFS Inventory (Legacy)](actions/get-wfs-inventory-legacy.md) | REST | `GET /v3/fulfillment/inventory` | [docs](https://developer.walmart.com/us-marketplace/reference/getwfsinventory#:~:text=Utilities-,WFS%20Inventory,-GET) |
| [List Carrier Methods](actions/list-carrier-methods.md) | REST | `GET /v3/settings/shipping/carriers` | [docs](https://developer.walmart.com/us-marketplace/reference/getcarriermethods) |
| [List Categories](actions/list-categories.md) | REST | `GET /v3/utilities/taxonomy/departments/:departmentId` | [docs](https://developer.walmart.com/us-marketplace/reference/getcategories) |
| [List Departments](actions/list-departments.md) | REST | `GET /v3/utilities/taxonomy/departments` | [docs](https://developer.walmart.com/us-marketplace/reference/getdepartmentlist) |
| [List Feed Statuses](actions/list-feed-statuses.md) | REST | `GET /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/getallfeedstatuses#:~:text=Utilities-,All%20feed%20statuses,-GET) |
| [List Fulfillment Centers](actions/list-fulfillment-centers.md) | REST | `GET /v3/settings/shipping/shipnodes` | [docs](https://developer.walmart.com/us-marketplace/reference/getallfulfillmentcenters) |
| [List Inbound Shipments](actions/list-inbound-shipments.md) | REST | `GET /v3/fulfillment/inbound-shipments` | [docs](https://developer.walmart.com/us-marketplace/reference/getinboundshipments) |
| [List Inventory Levels](actions/list-inventory-levels.md) | REST | `GET /v3/inventories` | [docs](https://developer.walmart.com/us-marketplace/reference/getmultinodeinventoryforallskuandallshipnodes) |
| [List Items](actions/list-items.md) | REST (nextCursor) | `GET /v3/items` | [docs](https://developer.walmart.com/us-marketplace/reference/getallitems) |
| [List Items - Simulation](actions/list-items-simulation.md) | REST (nextCursor) | `GET /v1/simulations/items` | [docs](https://developer.walmart.com/us-marketplace/reference/getallitems) |
| [List Price Incentive Items](actions/list-price-incentive-items.md) | REST | `GET /v3/price/incentives` | [docs](https://developer.walmart.com/global-marketplace/reference/getallincentives) |
| [List Released Orders](actions/list-released-orders.md) | REST | `GET /v3/orders/released` | [docs](https://developer.walmart.com/global-marketplace/reference/getallorders) |
| [List Returns](actions/list-returns.md) | REST | `GET /v3/returns` | [docs](https://developer.walmart.com/us-marketplace/reference/getreturns#:~:text=Utilities-,Returns,-GET) |
| [List Shipping Templates](actions/list-shipping-templates.md) | REST | `GET /v3/settings/shipping/templates` | [docs](https://developer.walmart.com/us-marketplace/reference/getallshippingtemplates) |
| [List Subscriptions](actions/list-subscriptions.md) | REST | `GET /v3/webhooks/subscriptions` | [docs](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions) |
| [List Supported Carriers](actions/list-supported-carriers.md) | REST | `GET /v3/shipping/labels/carriers` | [docs](https://developer.walmart.com/us-marketplace/reference/getcarriers) |
| [List 3PL Providers](actions/list3-pl-providers.md) | REST | `GET /v3/settings/shipping/3plproviders` | [docs](https://developer.walmart.com/us-marketplace/reference/get3pfulfillmentproviders) |
| [Recon Report](actions/recon-report.md) | REST | `GET /v3/report/reconreport/reconFileJson` | [docs](https://developer.walmart.com/global-marketplace/reference/getallorders) |
| [Refund Order Lines](actions/refund-order-lines.md) | REST | `POST /v3/returns/:returnOrderId/refund` | [docs](https://developer.walmart.com/us-marketplace/reference/issuerefund) |
| [Retire an Item](actions/retire-an-item.md) | REST | `DELETE /v3/items/:sku` | [docs](https://developer.walmart.com/us-marketplace/reference/retireanitem) |
| [Search Seller Catalog](actions/search-seller-catalog.md) | REST | `POST /v3/items/catalog/search` | [docs](https://developer.walmart.com/us-marketplace/reference/getsearchresult) |
| [Search Walmart Catalog](actions/search-walmart-catalog.md) | REST | `GET /v3/items/walmart/search` | [docs](https://developer.walmart.com/us-marketplace/reference/getsearchresult) |
| [Ship Order Lines](actions/ship-order-lines.md) | REST | `POST /v3/orders/:purchaseOrderId/shipping` | [docs](https://developer.walmart.com/us-marketplace/reference/acknowledgeorders) |
| [Simulate Order Delivery](actions/simulate-order-delivery.md) | REST | `POST /v1/simulations/orders/:purchaseOrderId/deliver` | [docs](https://developer.walmart.com/us-marketplace/reference/simulatereturn) |
| [Simulate Return](actions/simulate-return.md) | REST | `POST v3/simulations/returns` | [docs](https://developer.walmart.com/us-marketplace/reference/simulatereturn) |
| [Bulk Order Setup - Simulation](actions/simulations-bulk-setup.md) | REST | `POST v1/simulations/bulk/orders` |  |
| [Stop Campaign](actions/stop-campaign.md) | REST | `PUT v3/advertising/sem/campaigns/:campaignId` | [docs](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails) |
| [Test Notification](actions/test-notification.md) | REST | `POST /v3/webhooks/test` | [docs](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions) |
| [Token API - authorization_code](actions/token-api-authorization-code.md) | REST | `POST v3/token` | [docs](https://developer.walmart.com/us-marketplace/reference/tokenapi) |
| [Token API - client_credentials](actions/token-api-client-credentials.md) | REST | `POST v3/token` | [docs](https://developer.walmart.com/us-marketplace/reference/tokenapi) |
| [Token API - refresh_token](actions/token-api-refresh-token.md) | REST | `POST v3/token` | [docs](https://developer.walmart.com/us-marketplace/reference/tokenapi) |
| [Update Inventory](actions/update-inventory.md) | REST | `PUT /v3/inventory` | [docs](https://developer.walmart.com/us-marketplace/reference/updateinventoryforanitem) |
| [Update Lag Time](actions/update-lag-time.md) | REST | `POST /v3/feeds` | [docs](https://developer.walmart.com/us-marketplace/reference/updatelagtimebulk) |
| [Update Shipment Tracking](actions/update-shipment-tracking.md) | REST | `POST v3/fulfillment/shipment-tracking` | [docs](https://developer.walmart.com/us-marketplace/reference/updateshipmenttrackingdetails) |
| [Update Subscription](actions/update-subscription.md) | REST | `PATCH /v3/webhooks/subscriptions/:subscriptionId` | [docs](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions) |
