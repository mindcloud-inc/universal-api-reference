# SmartRoutes: Native API Reference

A consolidated summary of SmartRoutes's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://api.smartroutes.io/v2/docs/api/
- **OpenAPI specification:** https://api.smartroutes.io/v2/docs/swagger.json
- **API base URL:** `https://api.smartroutes.io/v2`

## Authentication

### SmartRoutes Open API Key

Authenticate with a SmartRoutes Open API key generated from the Integrations menu after onboarding.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-access-key: <apiKey>
```

[Official authentication documentation](https://smartroutes.io/guides/integrations/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `page_info` in the query string as the pagination cursor.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Booking Availability](actions/check-booking-availability.md) | `POST /booking/availability` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Booking/paths/~1booking~1availability/post) |
| [Create Vehicle](actions/create-vehicle.md) | `POST /vehicles` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Vehicles/paths/~1vehicles/post) |
| [Delete Order By Number](actions/delete-order-by-number.md) | `DELETE /orders/order-number/:order_number` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Orders/paths/~1orders~1order-number~1{order_number}/delete) |
| [Delete Vehicle](actions/delete-vehicle.md) | `DELETE /vehicles/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Vehicles/paths/~1vehicles~1{id}/delete) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Customers/paths/~1customers~1{id}/get) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Orders/paths/~1orders~1{id}/get) |
| [Get Plan](actions/get-plan.md) | `GET /plans/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Plans/paths/~1plans~1{id}/get) |
| [Get Vehicle](actions/get-vehicle.md) | `GET /vehicles/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Vehicles/paths/~1vehicles~1{id}/get) |
| [List Capacities](actions/list-capacities.md) | `GET /capacities` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Capacities/paths/~1capacities/get) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Custom-Fields/paths/~1custom-fields/get) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Customers/paths/~1customers/get) |
| [List Notification Tasks](actions/list-notification-tasks.md) | `GET /notification-tasks` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Notification-Tasks/paths/~1notification-tasks/get) |
| [List Notification Templates](actions/list-notification-templates.md) | `GET /notifications/templates` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Notifications/paths/~1notifications~1templates/get) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Orders/paths/~1orders/get) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Plans/paths/~1plans/get) |
| [List Routes](actions/list-routes.md) | `GET /routes` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Routes/paths/~1routes/get) |
| [List Third Parties](actions/list-third-parties.md) | `GET /third-parties` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Third-Parties/paths/~1third-parties/get) |
| [List Vehicles](actions/list-vehicles.md) | `GET /vehicles` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Vehicles/paths/~1vehicles/get) |
| [List Zone Groups](actions/list-zone-groups.md) | `GET /zone-groups` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Zone-Groups/paths/~1zone-groups/get) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Customers/paths/~1customers~1{id}/put) |
| [Update Order](actions/update-order.md) | `PUT /orders/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Orders/paths/~1orders~1{id}/put) |
| [Update Vehicle](actions/update-vehicle.md) | `PUT /vehicles/:id` | [docs](https://api.smartroutes.io/v2/docs/api/#tag/Vehicles/paths/~1vehicles~1{id}/put) |
