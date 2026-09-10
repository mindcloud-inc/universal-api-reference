# <img src="https://images.mindcloud.co/apps/icons/brandmark-logo-acumatica-1_1782232690604.png" alt="Acumatica logo" width="28" height="28"> Acumatica: Universal API

An intuitive Cloud ERP system to power your whole business.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/acumatica/latest
- **Category:** Commerce / ERP
- **Actions:** 59
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.acumatica.com/
- **Vendor API docs:** https://help.acumatica.com/Help?ScreenId=ShowWiki&pageid=91dda8ed-5e92-48a5-a176-9a255506d0d6

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Acumatica Endpoints](actions/get-acumatica-erp-endpoints.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-acumatica-erp-endpoints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (59)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill](actions/get-bill.md) | GET |  |
| [List Bills](actions/list-bills.md) | GET |  |
| [Reverse Bill](actions/reverse-bill.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Contact](actions/create-or-update-contact.md) | PUT |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Customer](actions/create-or-update-customer.md) | PUT |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |

### Endpoints & Erp Version

| Action | Method | Description |
| --- | --- | --- |
| [List Acumatica Endpoints](actions/get-acumatica-erp-endpoints.md) | GET | Retrieve the Acumatica ERP Endpoints and the build version. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Inventory Adjustment](actions/inventory-adjustment.md) | PUT |  |
| [List Stock Items](actions/retrieve-stock-item.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Opportunity](actions/create-or-update-opportunity.md) | PUT |  |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST |  |
| [Get Payment](actions/list-payment-by-id.md) | GET |  |
| [List Payments](actions/list-payments.md) | GET |  |
| [Release Payment](actions/release-payment.md) | PUT |  |
| [Void Payment](actions/void-payment.md) | PUT |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a Payment Link for an Sales Order |

### Project Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Task](actions/get-project-task.md) | GET |  |
| [List Project Tasks](actions/list-project-tasks.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieve a base64 encoded file content using Acumatica the '/files/{id}' Endpoint. |
| [Get Project Balance](actions/get-project-balance.md) | GET |  |
| [Get Project by ID](actions/get-project-by-id.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Create Project](actions/new-action1.md) | POST |  |
| [Search By Entity](actions/search-by-entity.md) | GET | Search the 'Default' Acumatica Endpoint for a Specific Entity |
| [Search By Generic Inquiry](actions/search-by-generic-inquiry.md) | GET | Search the 'Default' Acumatica Endpoint for a Generic Inquiry. This need to be a PUT |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order](actions/get-purchase-order.md) | GET |  |
| [List Purchase Orders](actions/get-purchase-orders-list.md) | GET |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create/Update Shipment](actions/create-update-shipment.md) | PUT |  |
| [Purchase Receipt](actions/purchase-receipt.md) | PUT |  |
| [Release Purchase Receipt](actions/release-purchase-receipt.md) | PUT |  |

### Purchase Receipt

| Action | Method | Description |
| --- | --- | --- |
| [List Purchase Receipts](actions/get-purchase-receipt.md) | GET |  |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Sales Order](actions/cancel-sales-order.md) | PUT |  |
| [Create or Update Sales Order](actions/create-or-update-sales-order.md) | PUT |  |
| [Delete Sales Order](actions/delete-sales-order.md) | DELETE |  |
| [Reopen Sales Order](actions/reopen-sales-order.md) | PUT |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Quantity Available](actions/get-inventory-quantity-available.md) | PUT |  |
| [Get Sales Order](actions/get-sales-order.md) | GET |  |
| [List Sales Orders](actions/list-sales-orders.md) | GET |  |
| [Send Inventory Quantity(to Custom Field)](actions/send-inventory-quantityto-custom-field.md) | PUT |  |
| [Update Sales Order](actions/update-sales-order.md) | PUT |  |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity Schema](actions/entity-schema.md) | GET | Get a specific Entity schema from the 'Default' Acumatica Endpoint. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Shipment](actions/confirm-shipment.md) | PUT |  |
| [Correct Shipment](actions/correct-shipment.md) | PUT |  |
| [Get Shipment](actions/get-shipment.md) | GET |  |
| [List Shipments](actions/list-shipments.md) | GET |  |
| [Prepare Invoice from Shipment](actions/prepare-invoice-from-shipment.md) | POST |  |
| [Update Shipment Inventory](actions/update-shipment-inventory.md) | PUT |  |

### Stock Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Item](actions/get-stock-item.md) | GET |  |
| [Update Stock Item Standard Cost](actions/update-stock-item-standard-cost.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Task](actions/create-project-task.md) | POST |  |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor](actions/get-vendor.md) | GET |  |
| [List Vendors](actions/list-vendors.md) | GET |  |

