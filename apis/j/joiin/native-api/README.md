# Joiin: Native API Reference

A consolidated summary of Joiin's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://app.joiin.co/reference
- **OpenAPI specification:** https://app.joiin.co/assets/public-api.json
- **API base URL:** `https://app-api.joiin.co`

## Authentication

### API Key

Connect Joiin with a Public API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.joiin.co/support/solutions/articles/42000110771-joiin-connect-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /v1/companies` | [docs](https://app.joiin.co/reference/create_company) |
| [Delete Company](actions/delete-company.md) | `DELETE /v1/companies/:id` | [docs](https://app.joiin.co/reference/delete_company) |
| [List Companies](actions/list-companies.md) | `GET /v1/companies` | [docs](https://app.joiin.co/reference/list_companies) |
| [Run Balance Sheet Report](actions/run-balance-sheet-report.md) | `POST /v1/report/balance-sheet` | [docs](https://app.joiin.co/reference/run_balance_sheet_report) |
| [Run Cashflow Report](actions/run-cashflow-report.md) | `POST /v1/report/cashflow` | [docs](https://app.joiin.co/reference/run_cashflow_report) |
| [Run Custom Report](actions/run-custom-report.md) | `POST /v1/report/custom-report` | [docs](https://app.joiin.co/reference/run_custom_report) |
| [Run Profit and Loss Report](actions/run-profit-and-loss-report.md) | `POST /v1/report/profit-loss` | [docs](https://app.joiin.co/reference/run_profit_and_loss_report) |
| [Run Trial Balance Report](actions/run-trial-balance-report.md) | `POST /v1/report/trial-balance` | [docs](https://app.joiin.co/reference/run_trial_balance_report) |
| [Update Company](actions/update-company.md) | `PUT /v1/companies/:id` | [docs](https://app.joiin.co/reference/update_company) |
