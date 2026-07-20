# GoTeamup: Native API Reference

A consolidated summary of GoTeamup's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.goteamup.com/
- **API base URL:** `https://goteamup.com/api/v2`

## Authentication

### OAuth2

OAuth2 authorization for TeamUp users and businesses.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://goteamup.com/api/v2/auth/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://goteamup.com/api/v2/auth/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read_write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://goteamup.com/api/v2/auth/refresh_access_token.

[Official authentication documentation](https://docs.goteamup.com/guides/oauth)

## API conventions

Response data is read from `results`.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Customer Membership](actions/cancel-customer-membership.md) | `POST /customer_memberships/:id/cancel` | [docs](https://docs.goteamup.com/api-reference/endpoints/customer-memberships-cancel-create) |
| [Create Customer](actions/create-customer.md) | `POST /customers` |  |
| [Create Customer Membership](actions/create-customer-membership.md) | `POST /customer_memberships` |  |
| [Create Membership](actions/create-membership.md) | `POST /memberships` |  |
| [Create Offering Type Helper](actions/create-offering-type-helper.md) | `POST /offering_types` | [docs](https://docs.goteamup.com/api-reference/endpoints/offering-types-create) |
| [Create Order](actions/create-order.md) | `POST /store/orders` | [docs](https://docs.goteamup.com/api-reference/endpoints/orders) |
| [Get Customer Membership Usage](actions/get-customer-membership-usage.md) | `GET /customer_memberships/:id/usage` | [docs](https://docs.goteamup.com/api-reference/endpoints/customer-memberships-usage-retrieve) |
| [Get Membership Allotment](actions/get-membership-allotment.md) | `GET /memberships/:id/allotment` | [docs](https://docs.goteamup.com/api-reference/endpoints/memberships) |
| [Get Provider Entitlements](actions/get-provider-entitlements.md) | `GET /providers/:id/entitlements` | [docs](https://docs.goteamup.com/api-reference/endpoints/providers-entitlements) |
| [List Customer Forms](actions/list-customer-forms.md) | `GET /customer_forms` | [docs](https://docs.goteamup.com/api-reference/endpoints/customer-forms-list) |
| [List Customer Memberships](actions/list-customer-memberships.md) | `GET /customer_memberships` | [docs](https://docs.goteamup.com/api-reference/endpoints/customer-memberships) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.goteamup.com/api-reference/endpoints/customers) |
| [List Discount Codes](actions/list-discount-codes.md) | `GET /discount_codes` | [docs](https://docs.goteamup.com/api-reference/endpoints/discount-codes) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.goteamup.com/api-reference/endpoints/events-list) |
| [List Instructors](actions/list-instructors.md) | `GET /instructors` | [docs](https://docs.goteamup.com/api-reference/endpoints/instructors-list) |
| [List Membership Categories](actions/list-membership-categories.md) | `GET /membership_categories` |  |
| [List Memberships](actions/list-memberships.md) | `GET /memberships` |  |
| [List Offering Types Helper](actions/list-offering-types-helper.md) | `GET /offering_types` | [docs](https://docs.goteamup.com/api-reference/endpoints/offering-types-list) |
| [List Orders](actions/list-orders.md) | `GET /store/orders` | [docs](https://docs.goteamup.com/api-reference/endpoints/orders) |
| [List Products](actions/list-products.md) | `GET /store/products` | [docs](https://docs.goteamup.com/api-reference/endpoints/products) |
| [List Providers](actions/list-providers.md) | `GET /providers` | [docs](https://docs.goteamup.com/api-reference/endpoints/providers-list) |
| [List Venues](actions/list-venues.md) | `GET /venues` | [docs](https://docs.goteamup.com/api-reference/endpoints/venues-list) |
| [List Venues Helper](actions/list-venues-helper.md) | `GET /venues` | [docs](https://docs.goteamup.com/api-reference/endpoints/venues-list) |
| [List Waivers](actions/list-waivers.md) | `GET /waivers` | [docs](https://docs.goteamup.com/api-reference/endpoints/waivers-list) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/customers-retrieve) |
| [Retrieve Customer Membership](actions/retrieve-customer-membership.md) | `GET /customer_memberships/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/customer-memberships) |
| [Retrieve Instructor](actions/retrieve-instructor.md) | `GET /instructors/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/instructors-retrieve) |
| [Retrieve Instructor Availability](actions/retrieve-instructor-availability.md) | `GET /instructors/:id/availability` | [docs](https://docs.goteamup.com/api-reference/endpoints/instructors-availability) |
| [Retrieve Membership](actions/retrieve-membership.md) | `GET /memberships/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/memberships) |
| [Retrieve Order](actions/retrieve-order.md) | `GET /store/orders/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/store-orders-retrieve) |
| [Retrieve Provider](actions/retrieve-provider.md) | `GET /providers/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/providers-retrieve) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/customers-partial-update) |
| [Update Membership](actions/update-membership.md) | `PUT /memberships/:id` | [docs](https://docs.goteamup.com/api-reference/endpoints/memberships) |
