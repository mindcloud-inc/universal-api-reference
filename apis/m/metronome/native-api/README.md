# Metronome: Native API Reference

A consolidated summary of Metronome's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.metronome.com/api-reference/introduction
- **OpenAPI specification:** https://docs.metronome.com/openapi.json
- **API base URL:** `https://api.metronome.com`

## Authentication

### Bearer Token

Authenticate Metronome API requests with a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.metronome.com/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–100). Use `next_page` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Billable Metric](actions/create-billable-metric.md) | `POST /v1/billable-metrics/create` | [docs](https://docs.metronome.com/api-reference/billable-metrics/create-a-billable-metric) |
| [Create Contract](actions/create-contract.md) | `POST /v1/contracts/create` | [docs](https://docs.metronome.com/api-reference/contracts/create-a-contract) |
| [Create Customer](actions/create-customer.md) | `POST /v1/customers` | [docs](https://docs.metronome.com/api-reference/customers/create-a-customer) |
| [Edit Contract](actions/edit-contract.md) | `POST /v2/contracts/edit` | [docs](https://docs.metronome.com/api-reference/contracts/edit-a-contract) |
| [Get Batched Usage Data](actions/get-batched-usage-data.md) | `POST /v1/usage` | [docs](https://docs.metronome.com/api-reference/usage/get-batched-usage-data) |
| [Get Billable Metric](actions/get-billable-metric.md) | `GET /v1/billable-metrics/:billable_metric_id` | [docs](https://docs.metronome.com/api-reference/billable-metrics/get-a-billable-metric) |
| [Get Contract](actions/get-contract.md) | `POST /v2/contracts/get` | [docs](https://docs.metronome.com/api-reference/contracts/get-a-contract-v2) |
| [Get Customer](actions/get-customer.md) | `GET /v1/customers/:customer_id` | [docs](https://docs.metronome.com/api-reference/customers/get-a-customer) |
| [Get Customer Billing Provider Configurations](actions/get-customer-billing-provider-configurations.md) | `POST /v1/getCustomerBillingProviderConfigurations` | [docs](https://docs.metronome.com/api-reference/customers/fetch-billing-provider-configurations-for-a-customer) |
| [Get Customer Net Balance](actions/get-customer-net-balance.md) | `POST /v1/contracts/customerBalances/getNetBalance` | [docs](https://docs.metronome.com/api-reference/credits-and-commits/get-the-net-balance-of-a-customer) |
| [Get Invoice](actions/get-invoice.md) | `GET /v1/customers/:customer_id/invoices/:invoice_id` | [docs](https://docs.metronome.com/api-reference/invoices/get-an-invoice) |
| [Get Usage Data With Paginated Groupings](actions/get-usage-data-with-paginated-groupings.md) | `POST /v1/usage/groups` | [docs](https://docs.metronome.com/api-reference/usage/get-usage-data-with-paginated-groupings) |
| [Ingest Events](actions/ingest-events.md) | `POST /v1/ingest` | [docs](https://docs.metronome.com/api-reference/usage/ingest-events) |
| [List Billable Metrics](actions/list-billable-metrics.md) | `GET /v1/billable-metrics` | [docs](https://docs.metronome.com/api-reference/billable-metrics/list-all-billable-metrics) |
| [List Customer Balances](actions/list-customer-balances.md) | `POST /v1/contracts/customerBalances/list` | [docs](https://docs.metronome.com/api-reference/credits-and-commits/list-balances) |
| [List Customer Contracts](actions/list-customer-contracts.md) | `POST /v2/contracts/list` | [docs](https://docs.metronome.com/api-reference/contracts/list-customer-contracts-v2) |
| [List Customers](actions/list-customers.md) | `GET /v1/customers` | [docs](https://docs.metronome.com/api-reference/customers/list-customers) |
| [List Invoices](actions/list-invoices.md) | `GET /v1/customers/:customer_id/invoices` | [docs](https://docs.metronome.com/api-reference/invoices/list-invoices) |
| [Search Events](actions/search-events.md) | `POST /v1/events/search` | [docs](https://docs.metronome.com/api-reference/usage/search-events) |
| [Set Customer Billing Provider Configurations](actions/set-customer-billing-provider-configurations.md) | `POST /v1/setCustomerBillingProviderConfigurations` | [docs](https://docs.metronome.com/api-reference/customers/set-billing-provider-configurations-for-a-customer) |
| [Set Customer Ingest Aliases](actions/set-customer-ingest-aliases.md) | `POST /v1/customers/:customer_id/setIngestAliases` | [docs](https://docs.metronome.com/api-reference/customers/create-or-update-customer-ingest-aliases) |
| [Update Billable Metric](actions/update-billable-metric.md) | `PUT /v1/billable-metrics/:billable_metric_id` | [docs](https://docs.metronome.com/api-reference/billable-metrics/update-a-billable-metric) |
| [Update Customer Configuration](actions/update-customer-configuration.md) | `POST /v1/customers/:customer_id/updateConfig` | [docs](https://docs.metronome.com/api-reference/customers/update-a-customer-configuration) |
| [Update Customer Name](actions/update-customer-name.md) | `POST /v1/customers/:customer_id/setName` | [docs](https://docs.metronome.com/api-reference/customers/update-a-customer-name) |
