# <img src="https://images.mindcloud.co/apps/icons/datex-icon-set-v3_1764886175970.jpeg" alt="DateX (Legacy) logo" width="28" height="28"> DateX (Legacy): Universal API

DateX connects to Wavelength/SKU warehouse and fulfillment APIs for read-only operational data such as sales orders, shipments, inventory, materials, carriers, owners, and warehouses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dateX/latest
- **Category:** Commerce
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://datexcorp.com/
- **Vendor API docs:** https://sku-mindcloud-api.wavelength.host/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Echo Test](actions/echo-test.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/echo-test?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

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
| [Save Shipping Label](actions/save-shipping-label.md) | POST |  |

### Owner

| Action | Method | Description |
| --- | --- | --- |
| [List Owners](actions/list-owners.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Update Materials](actions/update-materials.md) | PUT |  |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Orders](actions/list-sales-orders.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST |  |

### Salesorder

| Action | Method | Description |
| --- | --- | --- |
| [Update Sales Order](actions/update-sales-order.md) | PUT |  |

### Shipmen

| Action | Method | Description |
| --- | --- | --- |
| [Update sale order shipment containers](actions/update-sale-order-shipment-containers.md) | PUT | Just the markup value, status gets updated automatically |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Shipments](actions/list-sales-shipments.md) | GET |  |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Update Shipment](actions/update-shipment.md) | PUT |  |

### Shipping Detail

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Details](actions/list-shipping-details.md) | GET |  |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET |  |

