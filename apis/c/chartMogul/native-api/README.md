# ChartMogul: Native API Reference

A consolidated summary of ChartMogul's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://dev.chartmogul.com/docs/introduction/
- **API base URL:** `https://api.chartmogul.com/v1`

## Authentication

### API Key (Basic Auth)

Use your ChartMogul API key as the username. Use the same API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://dev.chartmogul.com/docs/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `entries`. The next-page cursor is read from `cursor`.

## Pagination

Use `per_page` in the query string to set the page size (default 200; accepted range 1–200). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://dev.chartmogul.com/reference/activities/list/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://dev.chartmogul.com/reference/contacts/list/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://dev.chartmogul.com/reference/customers/list/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://dev.chartmogul.com/reference/invoices/list/) |
| [List Notes and Call Logs](actions/list-notes-and-call-logs.md) | `GET /customer_notes` | [docs](https://dev.chartmogul.com/reference/notes-and-call-logs/list/) |
| [List Opportunities](actions/list-opportunities.md) | `GET /opportunities` | [docs](https://dev.chartmogul.com/reference/opportunities/list/) |
| [List Plan Groups](actions/list-plan-groups.md) | `GET /plan_groups` | [docs](https://dev.chartmogul.com/reference/plan-groups/list/) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://dev.chartmogul.com/reference/plans/list/) |
| [List Plans in a Plan Group](actions/list-plans-in-a-plan-group.md) | `GET /plan_groups/:planGroupUuid/plans` | [docs](https://dev.chartmogul.com/reference/plan-groups/list-plans/) |
| [List Sources](actions/list-sources.md) | `GET /data_sources` | [docs](https://dev.chartmogul.com/reference/sources/list/) |
| [List Subscription Events](actions/list-subscription-events.md) | `GET /subscription_events` | [docs](https://dev.chartmogul.com/reference/subscription-events/list/) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://dev.chartmogul.com/reference/tasks/list/) |
| [Retrieve Account Details](actions/retrieve-account-details.md) | `GET /account` | [docs](https://dev.chartmogul.com/reference/retrieve-account/) |
| [Retrieve All Key Metrics](actions/retrieve-all-key-metrics.md) | `GET /metrics/all` | [docs](https://dev.chartmogul.com/reference/metrics/all/) |
| [Retrieve ARR](actions/retrieve-arr.md) | `GET /metrics/arr` | [docs](https://dev.chartmogul.com/reference/metrics/arr/) |
| [Retrieve Average Revenue Per Account (ARPA)](actions/retrieve-average-revenue-per-account-arpa.md) | `GET /metrics/arpa` | [docs](https://dev.chartmogul.com/reference/metrics/arpa/) |
| [Retrieve Average Sale Price (ASP)](actions/retrieve-average-sale-price-asp.md) | `GET /metrics/asp` | [docs](https://dev.chartmogul.com/reference/metrics/asp/) |
| [Retrieve Customer Churn Rate](actions/retrieve-customer-churn-rate.md) | `GET /metrics/customer-churn-rate` | [docs](https://dev.chartmogul.com/reference/metrics/churn-rate/) |
| [Retrieve Customer Count](actions/retrieve-customer-count.md) | `GET /metrics/customer-count` | [docs](https://dev.chartmogul.com/reference/metrics/customer-count/) |
| [Retrieve LTV](actions/retrieve-ltv.md) | `GET /metrics/ltv` | [docs](https://dev.chartmogul.com/reference/metrics/ltv/) |
| [Retrieve MRR](actions/retrieve-mrr.md) | `GET /metrics/mrr` | [docs](https://dev.chartmogul.com/reference/metrics/mrr/) |
| [Retrieve MRR Churn Rate](actions/retrieve-mrr-churn-rate.md) | `GET /metrics/mrr-churn-rate` | [docs](https://dev.chartmogul.com/reference/metrics/mrr-churn-rate/) |
| [Retrieve Source](actions/retrieve-source.md) | `GET /data_sources/:dataSourceUuid` | [docs](https://dev.chartmogul.com/reference/sources/retrieve/) |
