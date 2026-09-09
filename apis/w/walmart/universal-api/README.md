# <img src="https://images.mindcloud.co/apps/icons/walmart_1782741049570.png" alt="Walmart logo" width="28" height="28"> Walmart: Universal API

Walmart through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/walmart/latest
- **Category:** Commerce
- **Actions:** 90
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seller.walmart.com/
- **Vendor API docs:** https://developer.walmart.com/us-marketplace/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Detail](actions/get-token-detail.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-token-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (90)

### Advertising

| Action | Method | Description |
| --- | --- | --- |
| [Check Eligibility of Items](actions/check-eligibility-of-items.md) | GET | Check whether an item from your catalog meets the required conditions for Search Engine Marketing ads. |
| [Create Campaign](actions/create-campaign.md) | POST | This API allows you to create a new Campaign. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Permanently remove an existing Campaign from the system. |
| [Get Campaign Details](actions/get-campaign-details.md) | GET | Retrieve detailed information about a specific Campaign. Provide the Campaign's unique ID in the request to fetch its attributes. |
| [Get Top Recommended Catalog Items](actions/get-top-recommended-catalog-items.md) | GET | This API allows you to fetch a list of top recommended items from your catalog. |
| [Stop Campaign](actions/stop-campaign.md) | PUT | This API allows you to stop an active Campaign. |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Detail](actions/get-token-detail.md) | GET | Returns OAuth token metadata and scopes granted by the seller to your application. Use this to verify whether a token is valid, when it… |
| [Token API - authorization_code](actions/token-api-authorization-code.md) | PUT |  |
| [Token API - client_credentials](actions/token-api-client-credentials.md) | POST |  |
| [Token API - refresh_token](actions/token-api-refresh-token.md) | PUT |  |

### Feed Management

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Error Report](actions/get-feed-error-report.md) | GET | Download a detailed error report for a submitted feed. |
| [Get Feed Item Status](actions/get-feed-item-status.md) | GET | Returns the overall feed status and item-level ingestion details for the specified feed. |
| [List Feed Statuses](actions/list-feed-statuses.md) | GET | Returns the feed statuses for all the specified Feed IDs. |

### Fulfillment Management

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Item Setup - WFS](actions/bulk-item-setup-wfs.md) | POST | This API is used for converting existing Marketplace items to be WFS eligible. |
| [Cancel Inbound Shipment](actions/cancel-inbound-shipment.md) | DELETE | Cancel an inbound shipment order. |
| [Get Inbound Shipment Errors](actions/get-inbound-shipment-errors.md) | GET | Retrieve a list of errors for an inbound shipment request. |
| [Get Inbound Shipment Items](actions/get-inbound-shipment-items.md) | GET | Retrieve a list of inbound shipments with optional filters. |
| [List Inbound Shipments](actions/list-inbound-shipments.md) | GET | Retrieve a list of inbound shipments with optional filters. |
| [Update Shipment Tracking](actions/update-shipment-tracking.md) | PUT | Enter Carrier and Tracking information for shipments. |

### Inventory Management

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Item Inventory Update](actions/bulk-item-inventory-update.md) | PUT | Upload a feed file to update inventory for multiple SKUs. |
| [Get Inventory](actions/get-inventory.md) | GET | Retrieve the current inventory for a single SKU. |
| [Get Single Item Inventory by Ship Node](actions/get-single-item-inventory-by-ship-node.md) | GET | Retrieve the current stock for one SKU at one or multiple ship nodes. |
| [Get WFS Inventory](actions/get-wfs-inventory.md) | GET |  |
| [Get WFS Inventory (Legacy)](actions/get-wfs-inventory-legacy.md) | GET |  |
| [List Inventory Levels](actions/list-inventory-levels.md) | GET | Retrieve the inventory level for every SKU at every ship node. |
| [Update Inventory](actions/update-inventory.md) | PUT | Replace the stock level for one SKU. |

### Item Management

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Item Setup - Delete Items](actions/bulk-item-setup-delete-items.md) | POST | Delete seller-fulfilled items from your catalog. |
| [Bulk Item Setup (multiple)](actions/bulk-item-setup-multiple.md) | POST | Set up a new seller fulfilled item. |
| [Bulk Item Setup - Retire Items](actions/bulk-item-setup-retire-items.md) | PUT | Permanently retire a list of Items identified by their SKU. |
| [Bulk Item Setup - Seller Fulfilled](actions/bulk-item-setup-seller-fulfilled.md) | POST | This API updates items in bulk (max: 10,000 items per request) |
| [Get Item](actions/get-item.md) | GET | Retrieved detailed information about a specific item from the partner's catalog. |
| [Get Item Associations](actions/get-item-associations.md) | GET | Retrieve Shipping Templates and Fulfillment Centers associated with your item SKUs. |
| [Get Item Count by Groups](actions/get-item-count-by-groups.md) | GET | Retrieve the total number of items based on variant group information. |
| [Get Item Count by Status](actions/get-item-count-by-status.md) | GET | Retrieve the total number of items filtered by a specific status. |
| [Get Spec](actions/get-spec.md) | GET | Retrieve specifications for a specified Product Type or a set of Product Types. |
| [Get Taxonomy](actions/get-taxonomy.md) | GET | Retrieve items taxonomy information. |
| [List Items](actions/list-items.md) | GET | Retrieve all items from a partner’s catalog. |
| [Retire an Item](actions/retire-an-item.md) | DELETE | Permanently retire an item identified by its SKU. |
| [Search Seller Catalog](actions/search-seller-catalog.md) | GET | Search your seller catalog with optional filters like Price, Listing Status, Rating etc. |
| [Search Walmart Catalog](actions/search-walmart-catalog.md) | GET | Search the Walmart.com global product catalog by item keyword, UPC or GTIN. |

### Lag Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Lag Time](actions/get-lag-time.md) | GET | Rretrieve Lag Time for an item with a given SKU. |
| [Update Lag Time](actions/update-lag-time.md) | PUT | Update of lag time for items in bulk. |

### Notifications Management

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Create one or more webhook subscriptions for event notifications by selecting an event type, event version, resource name, and providing a… |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Delete an existing webhook subscription by ID. |
| [Get Event Types](actions/get-event-types.md) | GET | Retrieve the list of event types and resource names available for subscription. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieve details of all webhook subscriptions you've created. |
| [Test Notification](actions/test-notification.md) | POST | Send a test notification to a destination URL using a sample payload. |
| [Update Subscription](actions/update-subscription.md) | POST | Update the details of a subscription. |

### Order Management

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Orders](actions/acknowledge-orders.md) | PUT | Acknowledge an entire order, including all of its order lines. |
| [Available Recon Report Dates](actions/available-recon-report-dates.md) | GET | Retrieves details of all orders with optional search criteria. |
| [Cancel Order Lines](actions/cancel-order-lines.md) | PUT | Cancel one or more order lines for a specific `purchaseOrderId`. |
| [List Orders](actions/get-all-orders.md) | GET | Retrieves details of all orders with optional search criteria. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order detail for a specific purchaseOrderId |
| [List Released Orders](actions/list-released-orders.md) | GET | Retrieves details of all orders with line items in the "created" status. |
| [Recon Report](actions/recon-report.md) | GET | Retrieves details of all orders with optional search criteria. |
| [Ship Order Lines](actions/ship-order-lines.md) | PUT | Marks specified order lines in a single purchase order as shipped. |

### Price & Promotion Management

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Price ( Legacy )](actions/bulk-update-price-legacy.md) | PUT | Updates prices in bulk. |
| [Bulk Update Price ( New )](actions/bulk-update-price-new.md) | PUT | Update the price section in bulk for multiple items. This is useful for implementing pricing strategies across your catalog, such as… |
| [Bulk Update Promotional Price](actions/bulk-update-promotional-price.md) | PUT | Create, update, or delete promotional prices for multiple SKUs. |
| [Get Promotional Prices](actions/get-promotional-prices.md) | GET | Retrieves a list of promotional prices for a single SKU. |
| [List Price Incentive Items](actions/list-price-incentive-items.md) | GET |  |

### Returns Management

| Action | Method | Description |
| --- | --- | --- |
| [List Returns](actions/list-returns.md) | GET | Retrieve details for return orders that match the filter criteria. |
| [Refund Order Lines](actions/refund-order-lines.md) | PUT | Issue refunds for return orders. |

### Settings Management

| Action | Method | Description |
| --- | --- | --- |
| [Create 3rd Party Fulfillment Center Association](actions/create3rd-party-fulfillment-center-association.md) | POST | Associate a third party fulfillment center with Seller. |
| [Delete Shipping Template](actions/delete-shipping-template.md) | DELETE | Delete Existing Shipping Template. |
| [Get Account Settings](actions/get-account-settings.md) | GET | https://developer.walmart.com/us-marketplace/reference/getaccountlevelsettings |
| [Get Fulfillment Center Coverages](actions/get-fulfillment-center-coverages.md) | GET | This API provides the list of all fullfillment centers for the seller and their coverage areas defined by Walmart based on the address. |
| [Get Partner Configurations](actions/get-partner-configurations.md) | GET | Retrieve partner configurations like Seller Account & feed throttling values |
| [Get Shipping Configurations](actions/get-shipping-configurations.md) | GET | Retrieve shipping configurations like Lag Time. |
| [Get Shipping Template Activation Status](actions/get-shipping-template-activation-status.md) | GET | Get the Activation Status of the Shipping Templates, which are set through Walmart Seller Center. |
| [Get Shipping Template Details](actions/get-shipping-template-details.md) | GET | Get Shipping Template Details of CUSTOM, DEFAULT & 3PL-specific templates. |
| [List Carrier Methods](actions/list-carrier-methods.md) | GET | Gets the available carrier methods |
| [List Fulfillment Centers](actions/list-fulfillment-centers.md) | GET | Provides a list of all the fulfillment centers |
| [List Shipping Templates](actions/list-shipping-templates.md) | GET | Get all the shipping templates for a Seller. |
| [List 3PL Providers](actions/list3-pl-providers.md) | GET | Get a list of all third party fulfillment providers. |

### Ship With Walmart

| Action | Method | Description |
| --- | --- | --- |
| [Discard Label](actions/discard-label.md) | DELETE | Mark a generated label as discarded. |
| [Download Label](actions/download-label.md) | GET | Retrieve the label for a carrier & tracking number combination. Returns PDF or PNG formatted label. |
| [Get Label Details](actions/get-label-details.md) | GET | Retrieves all label details generated for a purchase order id. |
| [Get Supported Carrier Package Types](actions/get-supported-carrier-package-types.md) | GET | Retrieves supported package types for a selected carrier. |
| [List Supported Carriers](actions/list-supported-carriers.md) | GET | Retrieves all carriers supported by Ship With Walmart. |

### Simplified Shipping Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Simplified Shipping Settings](actions/get-simplified-shipping-settings.md) | GET | Fetch the Simplified Shipping Settings for a seller account and FC level configurations. |

### Simulations

| Action | Method | Description |
| --- | --- | --- |
| [List Items - Simulation](actions/list-items-simulation.md) | GET | Retrieve all items from a partner’s catalog in the Dynamic Sandbox. |
| [Simulate Order Delivery](actions/simulate-order-delivery.md) | PUT | This request updates an order with delivery information in the Marketplace dynamic sandbox. |
| [Simulate Return](actions/simulate-return.md) | PUT | Simulates the return creation for a given customer order and line item. |
| [Bulk Order Setup - Simulation](actions/simulations-bulk-setup.md) | POST | Simulations: On-click API that does item setup and order setup for sellers in the Marketplace dynamic sandbox. |

### Utilities

| Action | Method | Description |
| --- | --- | --- |
| [Get Taxonomy by Spec](actions/get-taxonomy-by-spec.md) | GET | Retrieve a list of all Categories and Sub-categories that are available on Walmart.com for the Item spec version you specify. |
| [Get Walmart API Status](actions/get-walmart-api-status.md) | GET | Get all marketplace Apis status. |
| [List Categories](actions/list-categories.md) | GET | Retrieve a list of categories for a specific department. |
| [List Departments](actions/list-departments.md) | GET | Get a list of departments. |

### Walmart+

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Item Enrollment for Walmart+](actions/bulk-item-enrollment-for-walmart-plus.md) | PUT | Manage item participation in the Walmart+ program. |

