# retailCRM: Native API Reference

A consolidated summary of retailCRM's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://help.retailcrm.pro/Developers/Index
- **API base URL:** `{accountUrl}/api/v5`

## Authentication

### API Key

Use a retailCRM account URL and API key to access the REST API.

### Credentials

- **API Key:** `apiKey` · required
- **Account URL:** `accountUrl` · required · RetailCRM workspace URL, for example https://your-subdomain.retailcrm.pro.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.retailcrm.pro/Developers/ApiRules)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.totalPageCount`. The current page number is read from `pagination.currentPage`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 20–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path |
| --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers/create` |
| [Create Order](actions/create-order.md) | `POST /orders/create` |
| [Create Task](actions/create-task.md) | `POST /tasks/create` |
| [Get Customer](actions/get-customer.md) | `GET /customers/:externalId` |
| [Get Order](actions/get-order.md) | `GET /orders/:externalId` |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` |
| [Get User](actions/get-user.md) | `GET /users/:id` |
| [List Currencies](actions/list-currencies.md) | `GET /reference/currencies` |
| [List Customers](actions/list-customers.md) | `GET /customers` |
| [List Delivery Services](actions/list-delivery-services.md) | `GET /reference/delivery-services` |
| [List Delivery Types](actions/list-delivery-types.md) | `GET /reference/delivery-types` |
| [List Legal Entities](actions/list-legal-entities.md) | `GET /reference/legal-entities` |
| [List Offers](actions/list-offers.md) | `GET /store/offers` |
| [List Order Methods](actions/list-order-methods.md) | `GET /reference/order-methods` |
| [List Order Types](actions/list-order-types.md) | `GET /reference/order-types` |
| [List Orders](actions/list-orders.md) | `GET /orders` |
| [List Payment Statuses](actions/list-payment-statuses.md) | `GET /reference/payment-statuses` |
| [List Payment Types](actions/list-payment-types.md) | `GET /reference/payment-types` |
| [List Products](actions/list-products.md) | `GET /store/products` |
| [List Segments](actions/list-segments.md) | `GET /segments` |
| [List Sites](actions/list-sites.md) | `GET /reference/sites` |
| [List Status Groups](actions/list-status-groups.md) | `GET /reference/status-groups` |
| [List Statuses](actions/list-statuses.md) | `GET /reference/statuses` |
| [List Stores](actions/list-stores.md) | `GET /reference/stores` |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` |
| [List Users](actions/list-users.md) | `GET /users` |
| [Update Customer](actions/update-customer.md) | `POST /customers/:externalId/edit` |
| [Update Order](actions/update-order.md) | `POST /orders/:externalId/edit` |
| [Update Task](actions/update-task.md) | `POST /tasks/:id/edit` |
