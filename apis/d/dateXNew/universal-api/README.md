# <img src="https://images.mindcloud.co/apps/icons/date-x_1776878914960.png" alt="DateX logo" width="28" height="28"> DateX: Universal API

DateX connects to Wavelength/SKU warehouse and fulfillment APIs for read-only operational data such as sales orders, shipments, inventory, materials, carriers, owners, and warehouses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dateXNew/latest
- **Category:** Commerce
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datexcorp.com/
- **Vendor API docs:** https://sku-mindcloud-api.wavelength.host/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Echo Test](actions/echo-test.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/echo-test?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Available Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List Available Inventory](actions/list-available-inventory.md) | GET |  |

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [List Carriers](actions/list-carriers.md) | GET |  |

### Echo

| Action | Method | Description |
| --- | --- | --- |
| [Echo Test](actions/echo-test.md) | GET |  |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory](actions/list-inventory.md) | GET |  |

### Material

| Action | Method | Description |
| --- | --- | --- |
| [List Materials](actions/list-materials.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authorize](actions/authorize.md) | POST |  |

### Owner

| Action | Method | Description |
| --- | --- | --- |
| [List Owners](actions/list-owners.md) | GET |  |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Orders](actions/create-sales-orders.md) | POST |  |
| [List Sales Orders](actions/list-sales-orders.md) | GET |  |
| [Update Sales Orders](actions/update-sales-orders.md) | PUT |  |

### Sales Order Line

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order Lines](actions/create-sales-order-lines.md) | POST |  |
| [Update Sales Order Lines](actions/update-sales-order-lines.md) | PUT |  |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Shipments](actions/list-sales-shipments.md) | GET |  |
| [Update Shipment Markup Cost](actions/update-shipment-markup-cost.md) | PUT |  |

### Shipment Transmission

| Action | Method | Description |
| --- | --- | --- |
| [Delete Shipment Transmissions](actions/delete-shipment-transmissions.md) | DELETE |  |

### Shipping Detail

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Details](actions/list-shipping-details.md) | GET |  |
| [Update Shipping Details](actions/update-shipping-details.md) | PUT |  |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET |  |

