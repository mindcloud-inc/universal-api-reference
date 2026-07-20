# <img src="https://images.mindcloud.co/apps/icons/returnless_1775143532434.png" alt="Returnless logo" width="28" height="28"> Returnless: Universal API

Returnless REST API for operational return management, customers, shipments, products, and related support workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/returnless/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.returnless.com/
- **Vendor API docs:** https://docs.returnless.com/docs/api-rest-reference/64548cf9032b4

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account from Returnless. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Returnless. |
| [List Customer Addresses](actions/list-customer-addresses.md) | GET | Retrieves customer addresses from Returnless. |
| [List Customer Groups](actions/list-customer-groups.md) | GET | Retrieves customer groups from Returnless. |
| [List Customer Return Orders](actions/list-customer-return-orders.md) | GET | Retrieves customer return orders from Returnless. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Returnless. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Returnless. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Returnless. |

### Return Order

| Action | Method | Description |
| --- | --- | --- |
| [Add Return Order Item](actions/add-return-order-item.md) | PUT | Adds an item to a return order in Returnless. |
| [Add Return Order Note](actions/add-return-order-note.md) | PUT | Adds a note to a return order in Returnless. |
| [Add Return Order Shipment](actions/add-return-order-shipment.md) | PUT | Adds a shipment to a return order in Returnless. |
| [Approve Return Order](actions/approve-return-order.md) | PUT | Approves a return order in Returnless. |
| [Attach Return Order Tags](actions/attach-return-order-tags.md) | PUT | Attaches tags to a return order in Returnless. |
| [Create Return Order](actions/create-return-order.md) | POST | Creates a new return order in Returnless. |
| [Detach Return Order Tags](actions/detach-return-order-tags.md) | DELETE | Detaches tags from a return order in Returnless. |
| [Get Return Order](actions/get-return-order.md) | GET | Retrieves a return order from Returnless. |
| [List Return Order Items](actions/list-return-order-items.md) | GET | Retrieves return order items from Returnless. |
| [List Return Order Metadata](actions/list-return-order-metadata.md) | GET | Retrieves return order metadata from Returnless. |
| [List Return Order Notes](actions/list-return-order-notes.md) | GET | Retrieves return order notes from Returnless. |
| [List Return Order Shipments](actions/list-return-order-shipments.md) | GET | Retrieves return order shipments from Returnless. |
| [List Return Order Tags](actions/list-return-order-tags.md) | GET | Retrieves return order tags from Returnless. |
| [List Return Orders](actions/list-return-orders.md) | GET | Retrieves return orders from Returnless. |
| [Reject Return Order](actions/reject-return-order.md) | PUT | Rejects a return order in Returnless. |
| [Update Return Order Metadata](actions/update-return-order-metadata.md) | PUT | Updates return order metadata in Returnless. |
| [Update Return Order Status](actions/update-return-order-status.md) | PUT | Updates a return order status in Returnless. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Returnless. |
| [List Sales Order Items](actions/list-sales-order-items.md) | GET | Retrieves sales order items from Returnless. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from Returnless. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Returnless. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Returnless. |

