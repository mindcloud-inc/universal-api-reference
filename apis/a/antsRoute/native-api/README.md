# AntsRoute: Native API Reference

A consolidated summary of AntsRoute's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://app.antsroute.com/doc-api/index.html
- **OpenAPI specification:** https://app.antsroute.com/v3/api-docs/public
- **API base URL:** `https://app.antsroute.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
cakey: <apiKey>
```

[Official authentication documentation](https://support.antsroute.com/hc/en-gb/articles/4687507484817-Where-can-I-find-my-API-key-to-synchronize-my-data)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `size` in the query string to set the page size (default 10; maximum 500). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /capi/customer` | [docs](https://app.antsroute.com/doc-api/index.html#/Customer/createCustomer) |
| [Create Service/Delivery/Collect in Basket](actions/create-service-delivery-collect-in-basket.md) | `POST /capi/order/basket` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/createBasketOrder) |
| [Get Agent by Email](actions/get-agent-by-email.md) | `GET /capi/agent/:agentEmail` | [docs](https://app.antsroute.com/doc-api/index.html#/Agent/getAgent) |
| [Get Agent Last Known Position](actions/get-agent-last-known-position.md) | `GET /capi/agent/:agentEmail/last-known-position` | [docs](https://app.antsroute.com/doc-api/index.html#/Agent/getLastKnownPosition) |
| [Get Customer by External ID](actions/get-customer-by-external-id.md) | `GET /capi/customer/external-id/:externalId` | [docs](https://app.antsroute.com/doc-api/index.html#/Customer/getCustomerByExternalId) |
| [Get Customer by ID](actions/get-customer-by-id.md) | `GET /capi/customer/id/:id` | [docs](https://app.antsroute.com/doc-api/index.html#/Customer/getCustomerById) |
| [Get Order by External ID](actions/get-order-by-external-id.md) | `GET /capi/order/external-id/:externalId` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/getOrderByExternalId) |
| [Get Order by ID](actions/get-order-by-id.md) | `GET /capi/order/id/:id` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/getOrderById) |
| [Get Order Tracking Link](actions/get-order-tracking-link.md) | `GET /capi/order/id/:id/tracking-link` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/getTrackingLinkById) |
| [Get Route by Agent and Date](actions/get-route-by-agent-and-date.md) | `GET /capi/route/:agentEmail/:date` | [docs](https://app.antsroute.com/doc-api/index.html#/Route/getRouteByAgentEmailAndDate) |
| [List Agents](actions/list-agents.md) | `GET /capi/agent` | [docs](https://app.antsroute.com/doc-api/index.html#/Agent/getAllAgents) |
| [List Customer Orders](actions/list-customer-orders.md) | `GET /capi/customer/id/:id/orders` | [docs](https://app.antsroute.com/doc-api/index.html#/Customer/getCustomerOrdersById) |
| [List Customers](actions/list-customers.md) | `GET /capi/customer` | [docs](https://app.antsroute.com/doc-api/index.html#/Customer/findAllCustomers) |
| [List Orders](actions/list-orders.md) | `GET /capi/order` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/findOrder) |
| [List Routes by Date](actions/list-routes-by-date.md) | `GET /capi/route/:date` | [docs](https://app.antsroute.com/doc-api/index.html#/Route/getRoutesByDate) |
| [Search Order Availabilities](actions/search-order-availabilities.md) | `POST /capi/order/search-availabilities` | [docs](https://app.antsroute.com/doc-api/index.html#/Search%20availabilities%20and%20validate%20one%20in%20your%20planning/checkOrderAvailabilities) |
| [Update Customer by ID](actions/update-customer-by-id.md) | `PUT /capi/customer/id/:id` | [docs](https://app.antsroute.com/doc-api/index.html#/Customer/updateCustomer) |
| [Update Order by External ID](actions/update-order-by-external-id.md) | `PATCH /capi/order/external-id/:externalId` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/patchOrderByExternalId) |
| [Update Order by ID](actions/update-order-by-id.md) | `PATCH /capi/order/id/:id` | [docs](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/patchOrder) |
