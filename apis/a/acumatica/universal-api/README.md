# <img src="https://images.mindcloud.co/apps/icons/brandmark-logo-acumatica-1_1782232690604.png" alt="Acumatica logo" width="28" height="28"> Acumatica: Universal API

An intuitive Cloud ERP system to power your whole business.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/acumatica/latest
- **Category:** Commerce / ERP
- **Actions:** 27
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

## Actions (27)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create/Update Sales Orders](actions/create-update-sales-orders.md) | PUT |  |

### Endpoints & Erp Version

| Action | Method | Description |
| --- | --- | --- |
| [List Acumatica Endpoints](actions/get-acumatica-erp-endpoints.md) | GET | Retrieve the Acumatica ERP Endpoints and the build version. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Inventory Adjustment](actions/inventory-adjustment.md) | PUT |  |
| [Retrieve Stock Item](actions/retrieve-stock-item.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a Payment Link for an Sales Order |

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

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create/Update Shipment](actions/create-update-shipment.md) | PUT |  |
| [Get Purchase Receipt](actions/get-purchase-receipt.md) | GET |  |
| [Purchase Receipt](actions/purchase-receipt.md) | PUT |  |
| [Release Purchase Receipt](actions/release-purchase-receipt.md) | PUT |  |
| [Reopen Shipment](actions/reopen-shipment.md) | POST |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Shipment](actions/confirm-shipment.md) | PUT |  |
| [Get Inventory Quantity Available](actions/get-inventory-quantity-available.md) | PUT |  |
| [Get Purchase Order](actions/get-purchase-order.md) | GET |  |
| [Get Purchase Orders List](actions/get-purchase-orders-list.md) | GET |  |
| [Get Sales Order](actions/get-sales-order.md) | GET |  |
| [List Sales Orders](actions/list-sales-orders.md) | GET |  |
| [Send Inventory Quantity(to Custom Field)](actions/send-inventory-quantityto-custom-field.md) | PUT |  |
| [Update Sales Order](actions/update-sales-order.md) | PUT |  |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity Schema](actions/entity-schema.md) | GET | Get a specific Entity schema from the 'Default' Acumatica Endpoint. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Task](actions/create-project-task.md) | POST |  |

