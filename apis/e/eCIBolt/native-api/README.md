# ECI Bolt: Native API Reference

A consolidated summary of ECI Bolt's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.bolttech.net/api-docs/index.html
- **OpenAPI specification:** https://app.bolttech.net/api-docs/v1/swagger.yaml
- **API base URL:** `https://app.bolttech.net`

## Authentication

### API token

Connect with the API token and token name issued for your Bolt account.

### Credentials

- **API token:** `apiKey` · required
- **Token name:** `tokenName` · required · Enter the name paired with your Bolt API token. Both values are required by Bolt's Authorization header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.bolttech.net/company/open_api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextBatch`.

## Pagination

Use `next_batch` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /open/v1/customers` | [docs](https://app.bolttech.net/api-docs/index.html#/Customers/post_open_v1_customers) |
| [Create Job](actions/create-job.md) | `POST /open/v1/jobs` | [docs](https://app.bolttech.net/api-docs/index.html#/Jobs/post_open_v1_jobs) |
| [Create Work Order](actions/create-work-order.md) | `POST /open/v1/work_orders` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/post_open_v1_work_orders) |
| [Get Community](actions/get-community.md) | `GET /open/v1/communities/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Communities/get_open_v1_communities__id_) |
| [Get Customer](actions/get-customer.md) | `GET /open/v1/customers/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Customers/get_open_v1_customers__id_) |
| [Get Job](actions/get-job.md) | `GET /open/v1/jobs/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs__id_) |
| [Get Job Event Token](actions/get-job-event-token.md) | `GET /open/v1/jobs/events/at` | [docs](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs_events_at) |
| [Get Work Order](actions/get-work-order.md) | `GET /open/v1/work_orders/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders__id_) |
| [Get Work Order Event Token](actions/get-work-order-event-token.md) | `GET /open/v1/work_orders/events/at` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders_events_at) |
| [List Communities](actions/list-communities.md) | `GET /open/v1/communities` | [docs](https://app.bolttech.net/api-docs/index.html#/Communities/get_open_v1_communities) |
| [List Customers](actions/list-customers.md) | `GET /open/v1/customers` | [docs](https://app.bolttech.net/api-docs/index.html#/Customers/get_open_v1_customers) |
| [List Job Events](actions/list-job-events.md) | `GET /open/v1/jobs/events` | [docs](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs_events) |
| [List Job Work Orders](actions/list-job-work-orders.md) | `GET /open/v1/jobs/:id/work_orders` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_jobs__id__work_orders) |
| [List Jobs](actions/list-jobs.md) | `GET /open/v1/jobs` | [docs](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs) |
| [List Stages](actions/list-stages.md) | `GET /open/v1/stages` | [docs](https://app.bolttech.net/api-docs/index.html#/Stages/get_open_v1_stages) |
| [List Statuses](actions/list-statuses.md) | `GET /open/v1/work_order_statuses` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Order_Statuses/get_open_v1_work_order_statuses) |
| [List Work Order Events](actions/list-work-order-events.md) | `GET /open/v1/work_orders/events` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders_events) |
| [List Work Order Statuses](actions/list-work-order-statuses.md) | `GET /open/v1/work_orders/:id/statuses` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders__id__statuses) |
| [List Work Order Types](actions/list-work-order-types.md) | `GET /open/v1/work_order_types` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Order_Types/get_open_v1_work_order_types) |
| [List Work Orders](actions/list-work-orders.md) | `GET /open/v1/work_orders` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders) |
| [Update Customer](actions/update-customer.md) | `PATCH /open/v1/customers/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Customers/patch_open_v1_customers__id_) |
| [Update Job](actions/update-job.md) | `PATCH /open/v1/jobs/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Jobs/patch_open_v1_jobs__id_) |
| [Update Work Order](actions/update-work-order.md) | `PATCH /open/v1/work_orders/:id` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/patch_open_v1_work_orders__id_) |
| [Update Work Order Status](actions/update-work-order-status.md) | `PATCH /open/v1/work_orders/:id/statuses` | [docs](https://app.bolttech.net/api-docs/index.html#/Work_Orders/patch_open_v1_work_orders__id__statuses) |
