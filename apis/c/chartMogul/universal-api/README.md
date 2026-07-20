# <img src="https://images.mindcloud.co/apps/icons/chart-mogul_1773866895683.png" alt="ChartMogul logo" width="28" height="28"> ChartMogul: Universal API

Track subscription revenue, customers, and retention metrics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chartMogul/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chartmogul.com
- **Vendor API docs:** https://dev.chartmogul.com/docs/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account Details](actions/retrieve-account-details.md) | GET | Retrieves account details from ChartMogul. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from ChartMogul. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from ChartMogul. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from ChartMogul. |

### Customer Note

| Action | Method | Description |
| --- | --- | --- |
| [List Notes and Call Logs](actions/list-notes-and-call-logs.md) | GET | Retrieves notes and call logs from ChartMogul. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from ChartMogul. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve All Key Metrics](actions/retrieve-all-key-metrics.md) | GET | Retrieves all key metrics from ChartMogul. |
| [Retrieve ARR](actions/retrieve-arr.md) | GET | Retrieves ARR from ChartMogul. |
| [Retrieve Average Revenue Per Account (ARPA)](actions/retrieve-average-revenue-per-account-arpa.md) | GET | Retrieves ARPA from ChartMogul. |
| [Retrieve Average Sale Price (ASP)](actions/retrieve-average-sale-price-asp.md) | GET | Retrieves ASP from ChartMogul. |
| [Retrieve Customer Churn Rate](actions/retrieve-customer-churn-rate.md) | GET | Retrieves customer churn rate from ChartMogul. |
| [Retrieve Customer Count](actions/retrieve-customer-count.md) | GET | Retrieves customer count from ChartMogul. |
| [Retrieve LTV](actions/retrieve-ltv.md) | GET | Retrieves LTV from ChartMogul. |
| [Retrieve MRR](actions/retrieve-mrr.md) | GET | Retrieves MRR from ChartMogul. |
| [Retrieve MRR Churn Rate](actions/retrieve-mrr-churn-rate.md) | GET | Retrieves MRR churn rate from ChartMogul. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from ChartMogul. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from ChartMogul. |
| [List Plans in a Plan Group](actions/list-plans-in-a-plan-group.md) | GET | Retrieves plans in a plan group from ChartMogul. |

### Plan Group

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Groups](actions/list-plan-groups.md) | GET | Retrieves plan groups from ChartMogul. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from ChartMogul. |
| [Retrieve Source](actions/retrieve-source.md) | GET | Retrieves a source from ChartMogul. |

### Subscription Event

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Events](actions/list-subscription-events.md) | GET | Retrieves subscription events from ChartMogul. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from ChartMogul. |

