# <img src="https://images.mindcloud.co/apps/icons/salesrender-icon_1776890033905.png" alt="SalesRender logo" width="28" height="28"> SalesRender: Universal API

Manage SalesRender CRM data, orders, users, items, and settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesRender/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salesrender.com
- **Vendor API docs:** https://wiki.salesrender.com/en/home/plugin/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-customers?connectionId=$CONNECTION_ID&query=query%20%7B%20customersFetcher%20%7B%20customers%20%7B%20id%20email%20registeredAt%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Item Categories](actions/list-item-categories.md) | GET | Retrieves item categories from SalesRender. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from SalesRender. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from SalesRender. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in SalesRender. |
| [List Items](actions/list-items.md) | GET | Retrieves items from SalesRender. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in SalesRender. |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [List Offers](actions/list-offers.md) | GET | Retrieves offers from SalesRender. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in SalesRender. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from SalesRender. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in SalesRender. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from SalesRender. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from SalesRender. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from SalesRender. |

### Target

| Action | Method | Description |
| --- | --- | --- |
| [List Targets](actions/list-targets.md) | GET | Retrieves targets from SalesRender. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in SalesRender. |
| [List Users](actions/list-users.md) | GET | Retrieves users from SalesRender. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in SalesRender. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from SalesRender. |

