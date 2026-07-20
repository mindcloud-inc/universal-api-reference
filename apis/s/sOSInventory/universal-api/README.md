# <img src="https://images.mindcloud.co/apps/icons/s-osinventory_1773936725056.png" alt="SOS Inventory logo" width="28" height="28"> SOS Inventory: Universal API

Manage inventory, sales orders, purchasing, and manufacturing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sOSInventory/latest
- **Category:** Commerce
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sosinventory.com
- **Vendor API docs:** https://developer.sosinventory.com/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Locations](actions/list-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in SOS Inventory. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from SOS Inventory. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from SOS Inventory. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in SOS Inventory. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates an estimate in SOS Inventory. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves an estimate from SOS Inventory. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from SOS Inventory. |
| [Update Estimate](actions/update-estimate.md) | PUT | Updates an existing estimate in SOS Inventory. |

### Goods Receipts

| Action | Method | Description |
| --- | --- | --- |
| [List Item Receipts](actions/list-item-receipts.md) | GET | Retrieves item receipts from SOS Inventory. |

### Inventory Transfers

| Action | Method | Description |
| --- | --- | --- |
| [List Transfers](actions/list-transfers.md) | GET | Retrieves transfers from SOS Inventory. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in SOS Inventory. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from SOS Inventory. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from SOS Inventory. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in SOS Inventory. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates an item in SOS Inventory. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from SOS Inventory. |
| [List Items](actions/list-items.md) | GET | Retrieves items from SOS Inventory. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in SOS Inventory. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from SOS Inventory. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Transfer](actions/create-transfer.md) | POST | Creates a transfer in SOS Inventory. |
| [Get Transfer](actions/get-transfer.md) | GET | Retrieves a transfer from SOS Inventory. |
| [Update Transfer](actions/update-transfer.md) | PUT | Updates an existing transfer in SOS Inventory. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a purchase order in SOS Inventory. |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from SOS Inventory. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from SOS Inventory. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in SOS Inventory. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a sales order in SOS Inventory. |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from SOS Inventory. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from SOS Inventory. |
| [Update Sales Order](actions/update-sales-order.md) | PUT | Updates an existing sales order in SOS Inventory. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a shipment in SOS Inventory. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from SOS Inventory. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from SOS Inventory. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in SOS Inventory. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST | Creates a vendor in SOS Inventory. |
| [Get Vendor](actions/get-vendor.md) | GET | Retrieves a vendor from SOS Inventory. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves vendors from SOS Inventory. |
| [Update Vendor](actions/update-vendor.md) | PUT | Updates an existing vendor in SOS Inventory. |

