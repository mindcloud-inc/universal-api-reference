# Baremetrics: Native API Reference

A consolidated summary of Baremetrics's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.baremetrics.com/reference
- **API base URL:** `https://sandbox.baremetrics.com`

## Authentication

### API Key

Bearer API key authentication for Baremetrics.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.baremetrics.com/reference/authentication)

## Pagination

Use `per_page` in the query string to set the page size (default 30; maximum 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `PUT /v1/:source_id/subscriptions/:subscription_oid/cancel` | [docs](https://developers.baremetrics.com/reference/cancel-subscription) |
| [Create Customer](actions/create-customer.md) | `POST /v1/:source_id/customers` | [docs](https://developers.baremetrics.com/reference/create-customer) |
| [Create Plan](actions/create-plan.md) | `POST /v1/:source_id/plans` | [docs](https://developers.baremetrics.com/reference/create-plan) |
| [Create Segment](actions/create-segment.md) | `POST /v1/segments` | [docs](https://developers.baremetrics.com/reference/create-segment) |
| [Create Subscription](actions/create-subscription.md) | `POST /v1/:source_id/subscriptions` | [docs](https://developers.baremetrics.com/reference/create-subscription) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /v1/:source_id/customers/:oid` | [docs](https://developers.baremetrics.com/reference/delete-customer) |
| [Delete Plan](actions/delete-plan.md) | `DELETE /v1/:source_id/plans/:oid` | [docs](https://developers.baremetrics.com/reference/delete-plan) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /v1/:source_id/subscriptions/:oid` | [docs](https://developers.baremetrics.com/reference/delete-subscription) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://developers.baremetrics.com/reference/get-account) |
| [List Customer Events](actions/list-customer-events.md) | `GET /v1/:source_id/customers/:oid/events` | [docs](https://developers.baremetrics.com/reference/list-customer-events) |
| [List Customers](actions/list-customers.md) | `GET /v1/:source_id/customers` | [docs](https://developers.baremetrics.com/reference/list-customers) |
| [List Fields](actions/list-fields.md) | `GET /v1/segments/fields` | [docs](https://developers.baremetrics.com/reference/list-fields) |
| [List Plans](actions/list-plans.md) | `GET /v1/:source_id/plans` | [docs](https://developers.baremetrics.com/reference/list-plans) |
| [List Segments](actions/list-segments.md) | `GET /v1/segments` | [docs](https://developers.baremetrics.com/reference/list-segments) |
| [List Sources](actions/list-sources.md) | `GET /v1/sources` | [docs](https://developers.baremetrics.com/reference/sources) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/:source_id/subscriptions` | [docs](https://developers.baremetrics.com/reference/list-subscriptions) |
| [Search Segment](actions/search-segment.md) | `POST /v1/segments/search` | [docs](https://developers.baremetrics.com/reference/search-segment) |
| [Show Customer](actions/show-customer.md) | `GET /v1/:source_id/customers/:oid` | [docs](https://developers.baremetrics.com/reference/show-customer) |
| [Show Customers](actions/show-customers.md) | `GET /v1/metrics/:metric/customers` | [docs](https://developers.baremetrics.com/reference/show-customers) |
| [Show Metric](actions/show-metric.md) | `GET /v1/metrics/:metric` | [docs](https://developers.baremetrics.com/reference/show-metric) |
| [Show Plan](actions/show-plan.md) | `GET /v1/:source_id/plans/:oid` | [docs](https://developers.baremetrics.com/reference/show-plan) |
| [Show Plan Breakout](actions/show-plan-breakout.md) | `GET /v1/metrics/:metric/plans` | [docs](https://developers.baremetrics.com/reference/show-plan-breakout) |
| [Show Segment](actions/show-segment.md) | `GET /v1/segments/:id` | [docs](https://developers.baremetrics.com/reference/show-segment) |
| [Show Subscription](actions/show-subscription.md) | `GET /v1/:source_id/subscriptions/:oid` | [docs](https://developers.baremetrics.com/reference/show-subscription) |
| [Show Summary](actions/show-summary.md) | `GET /v1/metrics` | [docs](https://developers.baremetrics.com/reference/show-summary) |
| [Update Customer](actions/update-customer.md) | `PUT /v1/:source_id/customers/:customer_oid` | [docs](https://developers.baremetrics.com/reference/update-customer) |
| [Update Plan](actions/update-plan.md) | `PUT /v1/:source_id/plans/:plan_oid` | [docs](https://developers.baremetrics.com/reference/update-plan) |
| [Update Segment](actions/update-segment.md) | `PUT /v1/segments/:id` | [docs](https://developers.baremetrics.com/reference/update-segment) |
| [Update Subscription](actions/update-subscription.md) | `PUT /v1/:source_id/subscriptions/:subscription_oid` | [docs](https://developers.baremetrics.com/reference/update-subscription) |
