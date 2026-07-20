# <img src="https://images.mindcloud.co/apps/icons/ants-route_1775051977738.png" alt="AntsRoute logo" width="28" height="28"> AntsRoute: Universal API

Create routes, manage deliveries, and track field operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/antsRoute/latest
- **Category:** Support / Field Service
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://antsroute.com
- **Vendor API docs:** https://app.antsroute.com/doc-api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent by Email](actions/get-agent-by-email.md) | GET | Retrieves an agent from AntsRoute by email. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agent records from your AntsRoute site. |

### Agent Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Last Known Position](actions/get-agent-last-known-position.md) | GET | Retrieves an agent's last known position in AntsRoute. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in AntsRoute. |
| [Get Customer by External ID](actions/get-customer-by-external-id.md) | GET | Retrieves a customer from AntsRoute by external ID. |
| [Get Customer by ID](actions/get-customer-by-id.md) | GET | Retrieves a customer from AntsRoute by ID. |
| [List Customers](actions/list-customers.md) | GET | Finds customer records in your AntsRoute site. |
| [Update Customer by ID](actions/update-customer-by-id.md) | PUT | Updates an existing customer in AntsRoute by ID. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order by External ID](actions/get-order-by-external-id.md) | GET | Retrieves an order from AntsRoute by external ID. |
| [Get Order by ID](actions/get-order-by-id.md) | GET | Retrieves an order from AntsRoute by ID. |
| [Get Order Tracking Link](actions/get-order-tracking-link.md) | GET | Retrieves an order tracking link from AntsRoute by ID. |
| [List Customer Orders](actions/list-customer-orders.md) | GET | Finds orders in AntsRoute for a customer. |
| [List Orders](actions/list-orders.md) | GET | Finds orders in AntsRoute by selected criteria. |
| [Search Order Availabilities](actions/search-order-availabilities.md) | GET | Finds order availabilities in AntsRoute planning. |
| [Update Order by External ID](actions/update-order-by-external-id.md) | PUT | Updates an existing order in AntsRoute by external ID. |
| [Update Order by ID](actions/update-order-by-id.md) | PUT | Updates an existing order in AntsRoute by ID. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Service/Delivery/Collect in Basket](actions/create-service-delivery-collect-in-basket.md) | POST | Creates a new basket order in AntsRoute. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Get Route by Agent and Date](actions/get-route-by-agent-and-date.md) | GET | Retrieves an AntsRoute route by agent and date. |
| [List Routes by Date](actions/list-routes-by-date.md) | GET | Retrieves routes from AntsRoute for a date. |

