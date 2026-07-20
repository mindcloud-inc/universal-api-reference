# <img src="https://images.mindcloud.co/apps/icons/syntage_1776290886391.png" alt="Syntage logo" width="28" height="28"> Syntage: Universal API

Access Syntage entities, invoices, tax records, webhook activity, and financial insights from your Syntage organization.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/syntage/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.syntage.com
- **Vendor API docs:** https://docs.syntage.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Entities](actions/list-entities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Accounts Payable Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounts Payable Insight](actions/get-accounts-payable-insight.md) | GET | Retrieves accounts payable insight for an entity in Syntage. |

### Accounts Receivable Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounts Receivable Insight](actions/get-accounts-receivable-insight.md) | GET | Retrieves accounts receivable insight for an entity in Syntage. |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Get Credential](actions/get-credential.md) | GET | Retrieves a credential from Syntage. |
| [List Credentials](actions/list-credentials.md) | GET | Retrieves credentials from Syntage. |

### Employees Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Employees Insight](actions/get-employees-insight.md) | GET | Retrieves employee insight for an entity in Syntage. |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity](actions/get-entity.md) | GET | Retrieves an entity from Syntage. |
| [List Entities](actions/list-entities.md) | GET | Retrieves entities from Syntage. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Syntage. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Syntage. |

### Expenditures Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Expenditures Insight](actions/get-expenditures-insight.md) | GET | Retrieves expenditures insight for an entity in Syntage. |

### Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Get Extraction](actions/get-extraction.md) | GET | Retrieves an extraction from Syntage. |
| [List Extractions](actions/list-extractions.md) | GET | Retrieves extractions from Syntage. |

### Financial Ratios Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Ratios Insight](actions/get-financial-ratios-insight.md) | GET | Retrieves financial ratios insight for an entity in Syntage. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Syntage. |
| [List Entity Invoices](actions/list-entity-invoices.md) | GET | Retrieves invoices for an entity in Syntage. |

### Invoice Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Entity Invoice Line Items](actions/list-entity-invoice-line-items.md) | GET | Retrieves invoice line items for an entity in Syntage. |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Payment](actions/get-invoice-payment.md) | GET | Retrieves an invoice payment from Syntage. |
| [List Entity Invoice Payments](actions/list-entity-invoice-payments.md) | GET | Retrieves invoice payments for an entity in Syntage. |

### Sales Revenue Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Revenue Insight](actions/get-sales-revenue-insight.md) | GET | Retrieves sales revenue insight for an entity in Syntage. |

### Scheduler

| Action | Method | Description |
| --- | --- | --- |
| [Get Scheduler](actions/get-scheduler.md) | GET | Retrieves a scheduler from Syntage. |
| [List Schedulers](actions/list-schedulers.md) | GET | Retrieves schedulers from Syntage. |

### Tax Compliance Check

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Compliance Check](actions/get-tax-compliance-check.md) | GET | Retrieves a tax compliance check from Syntage. |
| [List Entity Tax Compliance Checks](actions/list-entity-tax-compliance-checks.md) | GET | Retrieves tax compliance checks for an entity in Syntage. |

### Tax Return

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Return](actions/get-tax-return.md) | GET | Retrieves a tax return from Syntage. |
| [List Entity Tax Returns](actions/list-entity-tax-returns.md) | GET | Retrieves tax returns for an entity in Syntage. |

### Tax Return Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Return Data](actions/get-tax-return-data.md) | GET | Retrieves tax return data from Syntage. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Syntage. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoints from Syntage. |

### Webhook Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Request](actions/get-webhook-request.md) | GET | Retrieves a webhook request from Syntage. |
| [List Webhook Requests](actions/list-webhook-requests.md) | GET | Retrieves webhook requests from Syntage. |

