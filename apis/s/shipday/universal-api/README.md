# <img src="https://images.mindcloud.co/apps/icons/shipday_1774018701306.png" alt="Shipday logo" width="28" height="28"> Shipday: Universal API

Manage Shipday delivery orders, carriers, and delivery status

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shipday/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.shipday.com
- **Vendor API docs:** https://docs.shipday.com/reference/shipday-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Active Orders](actions/list-active-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/list-active-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Availability](actions/availability.md) | GET | Checks on-demand service availability in Shipday. |

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [Add Carrier](actions/add-carrier.md) | POST | Creates a new carrier in Shipday. |
| [List Carriers](actions/list-carriers.md) | GET | Retrieves all available carriers from Shipday. |

### Delivery Progress

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Order Delivery Progress](actions/retrieve-order-delivery-progress.md) | GET | Retrieves order delivery progress from Shipday. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves an estimate from Shipday for an order. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Assign Order to Driver](actions/assign-order-to-driver.md) | PUT | Assigns an existing order to a driver in Shipday. |
| [Create Order](actions/create-order.md) | POST | Creates a new delivery order in Shipday. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from Shipday. |
| [List Active Orders](actions/list-active-orders.md) | GET | Retrieves active orders from Shipday. |
| [Retrieve Order Details](actions/retrieve-order-details.md) | GET | Retrieves order details from Shipday. |
| [Search Delivery Orders](actions/search-delivery-orders.md) | GET | Finds delivery orders in Shipday by query filters. |
| [Set Order Ready to Pickup](actions/set-order-ready-to-pickup.md) | PUT | Marks an existing order ready for pickup in Shipday. |
| [Unassign Order from Driver](actions/unassign-order-from-driver.md) | PUT | Unassigns an existing order from a driver in Shipday. |
| [Update Order Status](actions/update-order-status.md) | PUT | Updates an existing order status in Shipday. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves all available services from Shipday. |

