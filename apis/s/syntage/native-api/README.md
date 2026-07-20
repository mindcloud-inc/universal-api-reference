# Syntage: Native API Reference

A consolidated summary of Syntage's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.syntage.com/api-reference/introduction
- **OpenAPI specification:** https://api.syntage.com/openapi.yaml
- **API base URL:** `https://api.sandbox.syntage.com`

## Authentication

### X-API-Key

Authenticate to Syntage with the X-API-Key header using the production API key from the Syntage dashboard.

### Credentials

- **API Key:** `apiKey` · optional · Production Syntage API key sent in the X-API-Key header.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.syntage.com/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Accounts Payable Insight](actions/get-accounts-payable-insight.md) | `GET /entities/:entityId/insights/accounts-payable` | [docs](https://docs.syntage.com/api-reference/accounts-payable-insight/get-accounts-payable.md) |
| [Get Accounts Receivable Insight](actions/get-accounts-receivable-insight.md) | `GET /entities/:entityId/insights/accounts-receivable` | [docs](https://docs.syntage.com/api-reference/accounts-receivable-insight/get-accounts-receivable.md) |
| [Get Credential](actions/get-credential.md) | `GET /credentials/:id` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-credentials/retrieve-a-credential.md) |
| [Get Employees Insight](actions/get-employees-insight.md) | `GET /entities/:entityId/insights/employees` | [docs](https://docs.syntage.com/api-reference/employees-insight/get-employees.md) |
| [Get Entity](actions/get-entity.md) | `GET /entities/:entityId` | [docs](https://docs.syntage.com/api-reference/entities/retrieve-an-entity.md) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://docs.syntage.com/api-reference/events/retrieve-an-event.md) |
| [Get Expenditures Insight](actions/get-expenditures-insight.md) | `GET /entities/:entityId/insights/expenditures` | [docs](https://docs.syntage.com/api-reference/expenditures-insight/get-expenditures.md) |
| [Get Extraction](actions/get-extraction.md) | `GET /extractions/:id` | [docs](https://docs.syntage.com/api-reference/extractions/retrieve-an-extraction.md) |
| [Get Financial Ratios Insight](actions/get-financial-ratios-insight.md) | `GET /entities/:entityId/insights/financial-ratios` | [docs](https://docs.syntage.com/api-reference/financial-ratios-insight/get-financial-ratios.md) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-invoices/retrieve-an-invoice.md) |
| [Get Invoice Payment](actions/get-invoice-payment.md) | `GET /invoices/payments/:id` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-invoice-payments/retrieve-an-invoice-payment.md) |
| [Get Sales Revenue Insight](actions/get-sales-revenue-insight.md) | `GET /entities/:entityId/insights/sales-revenue` | [docs](https://docs.syntage.com/api-reference/sales-revenue-insight/get-sales-revenue.md) |
| [Get Scheduler](actions/get-scheduler.md) | `GET /schedulers/:id` | [docs](https://docs.syntage.com/api-reference/schedulers/retrieve-a-scheduler.md) |
| [Get Tax Compliance Check](actions/get-tax-compliance-check.md) | `GET /tax-compliance-checks/:id` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-tax-compliance-checks/retrieve-a-tax-compliance-check.md) |
| [Get Tax Return](actions/get-tax-return.md) | `GET /tax-returns/:id` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-tax-returns/retrieve-a-tax-return.md) |
| [Get Tax Return Data](actions/get-tax-return-data.md) | `GET /tax-returns/:id/data` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-tax-returns/retrieve-a-tax-return-data.md) |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | `GET /webhook-endpoints/:id` | [docs](https://docs.syntage.com/api-reference/webhook-endpoints/retrieve-a-webhook-endpoint.md) |
| [Get Webhook Request](actions/get-webhook-request.md) | `GET /webhook-requests/:id` | [docs](https://docs.syntage.com/api-reference/webhook-requests/retrieve-a-webhook-request.md) |
| [List Credentials](actions/list-credentials.md) | `GET /credentials` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-credentials/list-all-credentials.md) |
| [List Entities](actions/list-entities.md) | `GET /entities` | [docs](https://docs.syntage.com/api-reference/entities/list-all-entities) |
| [List Entity Invoice Line Items](actions/list-entity-invoice-line-items.md) | `GET /entities/:entityId/invoices/line-items` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-invoice-line-items/list-all-entity-line-items.md) |
| [List Entity Invoice Payments](actions/list-entity-invoice-payments.md) | `GET /entities/:entityId/invoices/payments` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-invoice-payments/list-taxpayers-invoice-payments.md) |
| [List Entity Invoices](actions/list-entity-invoices.md) | `GET /entities/:entityId/invoices` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-invoices/list-all-taxpayers-invoices.md) |
| [List Entity Tax Compliance Checks](actions/list-entity-tax-compliance-checks.md) | `GET /entities/:entityId/tax-compliance-checks` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-tax-compliance-checks/list-all-taxpayers-tax-compliance-checks.md) |
| [List Entity Tax Returns](actions/list-entity-tax-returns.md) | `GET /entities/:entityId/tax-returns` | [docs](https://docs.syntage.com/api-reference/ds-mx-sat-tax-returns/list-all-taxpayers-tax-returns.md) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.syntage.com/api-reference/events/list-all-events.md) |
| [List Extractions](actions/list-extractions.md) | `GET /extractions` | [docs](https://docs.syntage.com/api-reference/extractions/list-all-extractions.md) |
| [List Schedulers](actions/list-schedulers.md) | `GET /schedulers` | [docs](https://docs.syntage.com/api-reference/schedulers/list-schedulers.md) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /webhook-endpoints` | [docs](https://docs.syntage.com/api-reference/webhook-endpoints/list-all-webhook-endpoints.md) |
| [List Webhook Requests](actions/list-webhook-requests.md) | `GET /webhook-requests` | [docs](https://docs.syntage.com/api-reference/webhook-requests/list-all-webhook-requests.md) |
