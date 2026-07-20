# <img src="https://images.mindcloud.co/apps/icons/fiddle_1775491707534.png" alt="Fiddle logo" width="28" height="28"> Fiddle: Universal API

Manage inventory, manufacturing, orders, and supply chain operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fiddle/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fiddle.io/
- **Vendor API docs:** https://fiddle.io/rest/api/v2/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inventory Types](actions/list-inventory-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Fiddle. |
| [Find Customer by ID](actions/find-customer-by-id.md) | GET | Finds a customer in Fiddle by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from the Fiddle account. |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Items](actions/list-inventory-items.md) | GET | Retrieves inventory item records from Fiddle. |

### Inventory Location

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Locations](actions/list-inventory-locations.md) | GET | Retrieves inventory location records from Fiddle. |

### Inventory Lot

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Lots](actions/list-inventory-lots.md) | GET | Retrieves inventory lot records from Fiddle. |
| [List Quarantined Lots](actions/list-quarantined-lots.md) | GET | Retrieves quarantined inventory lots from Fiddle. |

### Inventory Type

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Types](actions/list-inventory-types.md) | GET | Retrieves inventory type records from Fiddle. |

### Measurement Unit

| Action | Method | Description |
| --- | --- | --- |
| [List Measurement Units](actions/list-measurement-units.md) | GET | Retrieves measurement unit records from Fiddle. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in Fiddle. |
| [Find Purchase Order by ID](actions/find-purchase-order-by-id.md) | GET | Finds a purchase order in Fiddle by ID. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase order records from Fiddle. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in Fiddle. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales order records from Fiddle. |

### Sales Order Item

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Order Items](actions/list-sales-order-items.md) | GET | Retrieves sales order items from Fiddle. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST | Creates a new supplier in Fiddle. |
| [Find Supplier by ID](actions/find-supplier-by-id.md) | GET | Finds a supplier in Fiddle by ID. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves supplier records from the Fiddle account. |
| [Update Supplier](actions/update-supplier.md) | PUT | Updates an existing supplier in Fiddle. |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves work order records from Fiddle. |

