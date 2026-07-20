# <img src="https://images.mindcloud.co/apps/icons/amazon-1_1768252959060.png" alt="Amazon Seller logo" width="28" height="28"> Amazon Seller: Universal API

Manage Amazon listings, inventory, orders, and shipments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/amazonSeller/latest
- **Category:** Commerce
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://developer-docs.amazon.com/sp-api/reference/welcome-to-api-references

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Marketplace Participations](actions/get-marketplace-participations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-marketplace-participations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Catalog Items

| Action | Method | Description |
| --- | --- | --- |
| [Search Catalog Items by Identifier](actions/search-catalog-items-by-identifier.md) | GET | Finds catalog items in Amazon Seller by identifier. |

### Financial Event

| Action | Method | Description |
| --- | --- | --- |
| [List Financial Events by Order ID](actions/list-financial-events-by-order-id.md) | GET | Retrieves financial events for an Amazon Seller order. |

### Fulfillment By Amazon

| Action | Method | Description |
| --- | --- | --- |
| [Get FBA Inventory Summaries (AFN only)](actions/get-inventory-summaries.md) | GET | Retrieves AFN inventory summaries from Amazon Seller. |

### Fulfillment Inbound

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill of Lading](actions/get-bill-of-lading.md) | GET | Retrieves a shipment bill of lading from Amazon Seller. |
| [Get Inbound Plan](actions/get-inbound-plan.md) | GET | Retrieves an inbound plan from Amazon Seller. |
| [Get Labels](actions/get-labels.md) | GET | Retrieves inbound shipment labels from Amazon Seller. |
| [List Shipment Items](actions/get-shipment-items.md) | GET | Retrieves inbound shipment items from Amazon Seller. |
| [Get Shipment Items by ID](actions/get-shipment-items-by-id.md) | GET | Retrieves items from an Amazon Seller inbound shipment. |
| [List Inbound Plans](actions/list-inbound-plans.md) | GET | Retrieves inbound plans from Amazon Seller. |
| [List Shipments](actions/list-inbound-shipments.md) | GET | Retrieves inbound shipments from Amazon Seller. |
| [Update LTL Shipment Tracking Details](actions/update-ltl-shipment-tracking-details.md) | PUT | Updates LTL shipment tracking details in Amazon Seller. |
| [Update SPD Shipment Tracking Details](actions/update-spd-shipment-tracking-details.md) | PUT | Updates SPD shipment tracking details in Amazon Seller. |

### Listings

| Action | Method | Description |
| --- | --- | --- |
| [Get Listings Item](actions/get-listings-item.md) | GET | Retrieves a listings item from Amazon Seller. |
| [Patch Listings Item](actions/patch-listings-item.md) | PUT | Updates an existing listings item in Amazon Seller. |
| [Search Listings Items](actions/search-listings-items.md) | GET | Finds listings items in Amazon Seller. |

### Merchant Fulfillment Network

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Shipment](actions/cancel-shipment.md) | DELETE | Cancels a merchant fulfillment shipment in Amazon Seller. |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a merchant fulfillment shipment in Amazon Seller. |
| [Get Eligible Shipment Services](actions/get-eligible-shipment-services.md) | POST | Retrieves eligible shipping service offers from Amazon Seller. |
| [Get Shipment ( MFN )](actions/get-shipment-mfn.md) | GET | Retrieves a merchant fulfillment shipment from Amazon Seller. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Shipment](actions/confirm-shipment.md) | PUT | Updates shipment confirmation for an Amazon Seller order. |
| [Get Order Address](actions/get-order-address.md) | GET | Retrieves an order shipping address from Amazon Seller. |
| [Get Order Buyer Info](actions/get-order-buyer-info.md) | GET | Retrieves buyer information for an Amazon Seller order. |
| [Get Order Regulated Info](actions/get-order-regulated-info.md) | GET | Retrieves regulated information for an Amazon Seller order. |
| [Get Order](actions/get-order-v2026.md) | GET | Retrieves an order from Amazon Seller. |
| [Search Orders](actions/search-orders-v2026.md) | GET | Finds orders in Amazon Seller by creation or update time. |
| [Update Shipment Status](actions/update-shipment-status.md) | PUT | Updates shipment status for an Amazon Seller order. |
| [Update Verification Status](actions/update-verification-status.md) | PUT | Updates regulated order verification status in Amazon Seller. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create FBM Listings Inventory Report](actions/create-fbm-listings-inventory-report.md) | POST | Creates an FBM listings inventory report in Amazon Seller. |
| [Create Fulfillment Order](actions/create-fulfillment-order.md) | POST | Creates a fulfillment order in Amazon Seller. |
| [Get FBM Report Document](actions/get-fbm-report-document.md) | GET | Retrieves FBM report document details from Amazon Seller. |
| [Get FBM Report Status](actions/get-fbm-report-status.md) | GET | Retrieves FBM report details from Amazon Seller. |
| [Get Fulfillment Preview](actions/get-fulfillment-preview.md) | POST | Retrieves fulfillment order previews from Amazon Seller. |
| [List Settlement Report List](actions/list-settlement-report-list.md) | GET | Retrieves Settlement reports from Amazon Seller. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves finance transactions from Amazon Seller. |

### Sales

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Metrics](actions/get-order-metrics.md) | GET | Retrieves order metrics from Amazon Seller. |

### Sellers

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves seller account and marketplace details from Amazon Seller. |
| [Get Marketplace Participations](actions/get-marketplace-participations.md) | GET | Retrieves marketplace participations from Amazon Seller. |

