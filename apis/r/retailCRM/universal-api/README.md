# <img src="https://images.mindcloud.co/apps/icons/retail-crm_1776879403703.png" alt="retailCRM logo" width="28" height="28"> retailCRM: Universal API

Manage customers, orders, tasks, products, and retailCRM reference data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/retailCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.retailcrm.ru
- **Vendor API docs:** https://help.retailcrm.pro/Developers/Index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in retailCRM. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from retailCRM by external ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from retailCRM. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in retailCRM. |

### Fulfillments

| Action | Method | Description |
| --- | --- | --- |
| [List Delivery Services](actions/list-delivery-services.md) | GET | Retrieves delivery services from retailCRM. |
| [List Delivery Types](actions/list-delivery-types.md) | GET | Retrieves delivery types from retailCRM. |

### Legal Entities

| Action | Method | Description |
| --- | --- | --- |
| [List Legal Entities](actions/list-legal-entities.md) | GET | Retrieves legal entities from retailCRM. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from retailCRM. |
| [List Stores](actions/list-stores.md) | GET | Retrieves stores from retailCRM. |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [List Offers](actions/list-offers.md) | GET | Retrieves offers from retailCRM. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in retailCRM. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from retailCRM by external ID. |
| [List Order Methods](actions/list-order-methods.md) | GET | Retrieves order methods from retailCRM. |
| [List Order Types](actions/list-order-types.md) | GET | Retrieves order types from retailCRM. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from retailCRM. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in retailCRM. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Types](actions/list-payment-types.md) | GET | Retrieves payment types from retailCRM. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Statuses](actions/list-payment-statuses.md) | GET | Retrieves payment statuses from retailCRM. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from retailCRM. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from retailCRM. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from retailCRM. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Status Groups](actions/list-status-groups.md) | GET | Retrieves status groups from retailCRM. |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from retailCRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in retailCRM. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from retailCRM by ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from retailCRM. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in retailCRM. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from retailCRM by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves users from retailCRM. |

