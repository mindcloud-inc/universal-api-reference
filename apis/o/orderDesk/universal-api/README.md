# <img src="https://images.mindcloud.co/apps/icons/order-desk_1774035193710.png" alt="Order Desk logo" width="28" height="28"> Order Desk: Universal API

Manage orders, inventory, and shipments in Order Desk

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orderDesk/latest
- **Category:** Commerce
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.orderdesk.com/
- **Vendor API docs:** https://apidocs.orderdesk.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Store Settings](actions/get-store-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-store-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Inventory Item](actions/create-inventory-item.md) | POST | Creates a new inventory item in Order Desk. |
| [Delete Inventory Item](actions/delete-inventory-item.md) | DELETE | Deletes an existing inventory item from Order Desk. |
| [Get Inventory Item](actions/get-inventory-item.md) | GET | Retrieves an inventory item from Order Desk. |
| [List Inventory Items](actions/list-inventory-items.md) | GET | Retrieves inventory items from Order Desk. |
| [Update Inventory Item](actions/update-inventory-item.md) | PUT | Updates an existing inventory item in Order Desk. |
| [Update Multiple Inventory Items](actions/update-multiple-inventory-items.md) | PUT | Updates multiple inventory items in Order Desk. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Order Desk. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Order Desk. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Order Desk. |

### Order Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Item](actions/get-order-item.md) | GET | Retrieves an order item from Order Desk. |
| [List Order Items](actions/list-order-items.md) | GET | Retrieves order items from Order Desk. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple Shipments](actions/create-multiple-shipments.md) | POST | Creates multiple shipments in Order Desk. |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a new shipment in Order Desk. |
| [Delete Shipment](actions/delete-shipment.md) | DELETE | Deletes an existing shipment from Order Desk. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Order Desk. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Order Desk. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in Order Desk. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Store Settings](actions/get-store-settings.md) | GET | Retrieves store settings from Order Desk. |

