# <img src="https://images.mindcloud.co/apps/icons/amazon-1_1768252974873.png" alt="Amazon Vendor logo" width="28" height="28"> Amazon Vendor: Universal API

Amazon Vendor through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/amazonVendor/latest
- **Category:** Commerce
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.amazonservices.com/
- **Vendor API docs:** https://developer-docs.amazon.com/sp-api/reference/welcome-to-api-references

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Direct Fulfillment Packing Slip](actions/get-direct-fulfillment-packing-slip.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-packing-slip?connectionId=$CONNECTION_ID&purchaseOrderNumber=e.g.%20UvgABdBjQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Submit Inventory Update](actions/submit-inventory-update.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Submit Direct Fulfillment Invoices](actions/submit-direct-fulfillment-invoices.md) | POST |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Direct Fulfillment Packing Slip](actions/get-direct-fulfillment-packing-slip.md) | GET |  |
| [Get Order](actions/get-order.md) | GET |  |
| [Get Purchase Order](actions/get-purchase-order.md) | GET |  |
| [Get Purchase Orders](actions/get-purchase-orders.md) | GET |  |
| [List Direct Fulfillment Orders](actions/list-direct-fulfillment-orders.md) | GET |  |
| [Submit Direct Fulfillment Acknowledgements](actions/submit-direct-fulfillment-acknowledgements.md) | POST |  |
| [Submit Purchase Order Acknowledgements](actions/submit-purchase-order-acknowledgements.md) | POST |  |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Create Direct Fulfillment Shipping Labels](actions/create-direct-fulfillment-shipping-labels.md) | POST |  |
| [Get Direct Fulfillment Shipping Label](actions/get-direct-fulfillment-shipping-label.md) | GET |  |
| [Submit Direct Fulfillment Shipment Confirmations](actions/submit-direct-fulfillment-shipment-confirmations.md) | POST |  |
| [Submit Shipment Confirmations](actions/submit-shipment-confirmations.md) | POST |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Direct Fulfillment Transaction Status](actions/get-direct-fulfillment-transaction-status.md) | GET |  |
| [Get Transaction Status](actions/get-transaction-status.md) | GET |  |

