# <img src="https://images.mindcloud.co/apps/icons/metronome-logo-png-seeklogo-454949_1776785882041.png" alt="Metronome logo" width="28" height="28"> Metronome: Universal API

Manage customers, contracts, usage billing, invoices, and credits

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/metronome/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://metronome.com
- **Vendor API docs:** https://docs.metronome.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Billable Metric

| Action | Method | Description |
| --- | --- | --- |
| [Create Billable Metric](actions/create-billable-metric.md) | POST | Creates a new billable metric in Metronome. |
| [Get Billable Metric](actions/get-billable-metric.md) | GET | Retrieves a billable metric from Metronome. |
| [List Billable Metrics](actions/list-billable-metrics.md) | GET | Retrieves billable metrics from Metronome. |
| [Update Billable Metric](actions/update-billable-metric.md) | PUT | Updates an existing billable metric in Metronome. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract](actions/create-contract.md) | POST | Creates a new contract in Metronome. |
| [Edit Contract](actions/edit-contract.md) | PUT | Updates an existing contract in Metronome. |
| [Get Contract](actions/get-contract.md) | GET | Retrieves a contract from Metronome. |
| [List Customer Contracts](actions/list-customer-contracts.md) | GET | Retrieves contracts for a customer from Metronome. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Metronome. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Metronome. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Metronome. |
| [Set Customer Ingest Aliases](actions/set-customer-ingest-aliases.md) | PUT | Creates or updates customer ingest aliases in Metronome. |
| [Update Customer Configuration](actions/update-customer-configuration.md) | PUT | Updates a customer configuration in Metronome. |
| [Update Customer Name](actions/update-customer-name.md) | PUT | Updates a customer name in Metronome. |

### Customer Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Net Balance](actions/get-customer-net-balance.md) | GET | Retrieves a customer's net balance from Metronome. |
| [List Customer Balances](actions/list-customer-balances.md) | GET | Retrieves balances for a customer from Metronome. |

### Customer Billing Provider Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Billing Provider Configurations](actions/get-customer-billing-provider-configurations.md) | GET | Retrieves customer billing provider configurations from Metronome. |
| [Set Customer Billing Provider Configurations](actions/set-customer-billing-provider-configurations.md) | PUT | Updates customer billing provider configurations in Metronome. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Ingest Events](actions/ingest-events.md) | POST | Ingests events into Metronome. |
| [Search Events](actions/search-events.md) | GET | Finds events in Metronome by transaction ID. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Metronome. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Metronome. |

### Usage Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [Get Batched Usage Data](actions/get-batched-usage-data.md) | GET | Retrieves batched usage data from Metronome. |
| [Get Usage Data With Paginated Groupings](actions/get-usage-data-with-paginated-groupings.md) | GET | Retrieves paginated grouped usage data from Metronome. |

