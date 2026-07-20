# RO App: Native API Reference

A consolidated summary of RO App's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://roapp.readme.io/reference
- **API base URL:** `https://api.roapp.io/v2`

## Authentication

### Bearer API Key

Use an employee-scoped RO App API key from Settings > API. MindCloud sends it as Authorization: Bearer {{credentials.apiKey}}.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://roapp.readme.io/reference/getting-started-with-api)

## API conventions

The total page count is read from `paging.total_pages`. The current page number is read from `paging.page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 400 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://roapp.readme.io/reference/create-booking) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://roapp.readme.io/reference/create-estimate) |
| [Create Estimate Item](actions/create-estimate-item.md) | `POST /estimates/:estimate_id/items` | [docs](https://roapp.readme.io/reference/create-estimate-item) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://roapp.readme.io/reference/create-order) |
| [Create Order Item](actions/create-order-item.md) | `POST /orders/:order_id/items` | [docs](https://roapp.readme.io/reference/create-order-item) |
| [Create Organization](actions/create-organization.md) | `POST /contacts/organizations` | [docs](https://roapp.readme.io/reference/create-organization) |
| [Create Person](actions/create-person.md) | `POST /contacts/people` | [docs](https://roapp.readme.io/reference/create-person) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:booking_id` | [docs](https://roapp.readme.io/reference/get-booking-by-id) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://roapp.readme.io/reference/get-company) |
| [Get Estimate](actions/get-estimate.md) | `GET /estimates/:estimate_id` | [docs](https://roapp.readme.io/reference/get-estimate-by-id) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://roapp.readme.io/reference/get-invoice-by-id) |
| [Get Order](actions/get-order.md) | `GET /orders/:order_id` | [docs](https://roapp.readme.io/reference/get-order-by-id) |
| [Get Organization](actions/get-organization.md) | `GET /contacts/organizations/:organization_id` | [docs](https://roapp.readme.io/reference/get-organization-by-id) |
| [Get Person](actions/get-person.md) | `GET /contacts/people/:person_id` | [docs](https://roapp.readme.io/reference/get-person-by-id) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://roapp.readme.io/reference/get-bookigs) |
| [List Employees](actions/list-employees.md) | `GET /company/employees` | [docs](https://roapp.readme.io/reference/get-company-employees) |
| [List Estimate Items](actions/list-estimate-items.md) | `GET /estimates/:estimate_id/items` | [docs](https://roapp.readme.io/reference/get-estimate-items) |
| [List Estimate Statuses](actions/list-estimate-statuses.md) | `GET /estimates/statuses` | [docs](https://roapp.readme.io/reference/get-estimate-statuses) |
| [List Estimate Types](actions/list-estimate-types.md) | `GET /estimates/types` | [docs](https://roapp.readme.io/reference/get-estimates-types) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://roapp.readme.io/reference/get-estimates) |
| [List Invoice Items](actions/list-invoice-items.md) | `GET /invoices/:invoice_id/items` | [docs](https://roapp.readme.io/reference/get-invoice-items) |
| [List Invoice Statuses](actions/list-invoice-statuses.md) | `GET /invoices/statuses` | [docs](https://roapp.readme.io/reference/get-invoice-statuses) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://roapp.readme.io/reference/get-invoices) |
| [List Locations](actions/list-locations.md) | `GET /company/locations` | [docs](https://roapp.readme.io/reference/get-company-locations) |
| [List Order Items](actions/list-order-items.md) | `GET /orders/:order_id/items` | [docs](https://roapp.readme.io/reference/get-order-items) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /orders/statuses` | [docs](https://roapp.readme.io/reference/get-order-statuses) |
| [List Order Types](actions/list-order-types.md) | `GET /orders/types` | [docs](https://roapp.readme.io/reference/get-order-types) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://roapp.readme.io/reference/get-orders) |
| [List Organizations](actions/list-organizations.md) | `GET /contacts/organizations` | [docs](https://roapp.readme.io/reference/get-organizations) |
| [List People](actions/list-people.md) | `GET /contacts/people` | [docs](https://roapp.readme.io/reference/get-list-of-people) |
| [List Taxes](actions/list-taxes.md) | `GET /company/taxes` | [docs](https://roapp.readme.io/reference/get-taxes) |
| [Update Booking](actions/update-booking.md) | `PATCH /bookings/:booking_id` | [docs](https://roapp.readme.io/reference/update-booking) |
| [Update Estimate](actions/update-estimate.md) | `PATCH /estimates/:estimate_id` | [docs](https://roapp.readme.io/reference/update-estimate) |
| [Update Estimate Item](actions/update-estimate-item.md) | `PATCH /estimates/:estimate_id/items/:item_id` | [docs](https://roapp.readme.io/reference/update-estimate-item) |
| [Update Estimate Status](actions/update-estimate-status.md) | `POST /estimates/:estimate_id/status` | [docs](https://roapp.readme.io/reference/change-estimate-status) |
| [Update Order](actions/update-order.md) | `PATCH /orders/:order_id` | [docs](https://roapp.readme.io/reference/update-order) |
| [Update Order Item](actions/update-order-item.md) | `PATCH /orders/:order_id/items/:item_id` | [docs](https://roapp.readme.io/reference/update-order-item) |
| [Update Order Status](actions/update-order-status.md) | `POST /orders/:order_id/status` | [docs](https://roapp.readme.io/reference/update-order-status) |
| [Update Organization](actions/update-organization.md) | `PATCH /contacts/organizations/:organization_id` | [docs](https://roapp.readme.io/reference/update-organization) |
| [Update Person](actions/update-person.md) | `PATCH /contacts/people/:person_id` | [docs](https://roapp.readme.io/reference/update-person) |
