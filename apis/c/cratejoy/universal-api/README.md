# <img src="https://images.mindcloud.co/apps/icons/cratejoy_1775512696552.png" alt="Cratejoy logo" width="28" height="28"> Cratejoy: Universal API

Manage subscriptions, orders, shipments, and customers in Cratejoy

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cratejoy/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sell.cratejoy.com/
- **Vendor API docs:** https://docs.cratejoy.com/reference/introduction-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Address](actions/create-customer-address.md) | POST | Creates a customer address in Cratejoy. |
| [List Customer Addresses](actions/list-customer-addresses.md) | GET | Retrieves a customer's addresses from Cratejoy. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Cratejoy. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Cratejoy. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Cratejoy. |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Levels](actions/list-inventory-levels.md) | GET | Retrieves inventory levels from Cratejoy. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Cratejoy. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Cratejoy. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Cratejoy. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Cratejoy. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Cratejoy. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Cratejoy. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Cratejoy. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Cratejoy. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Cratejoy. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in Cratejoy. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels a subscription in Cratejoy. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Cratejoy. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Cratejoy. |
| [Reactivate Subscription](actions/reactivate-subscription.md) | PUT | Reactivates a subscription in Cratejoy. |
| [Skip Subscription](actions/skip-subscription.md) | PUT | Skips a subscription's next renewal in Cratejoy. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Cratejoy. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Cratejoy. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Cratejoy. |

