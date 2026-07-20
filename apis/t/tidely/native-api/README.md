# Tidely: Native API Reference

A consolidated summary of Tidely's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://faq.tidely.com/de/api-rechnungen
- **OpenAPI specification:** https://api.tidely.com/tidely-open-api-docs
- **API base URL:** `https://api.tidely.com`

## Authentication

### API Key (X-Authorization)

Use a Tidely API key. The app sends the raw value only in the X-Authorization header.

### Credentials

- **API Key:** `apiKey` · optional · Tidely API key value used for the X-Authorization header.

Send these headers with each API request:

```http
X-Authorization: <apiKey>
```

[Official authentication documentation](https://faq.tidely.com/de/zapier-integration)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add To Existing Period Plan](actions/add-to-existing-period-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Check Connection](actions/check-connection.md) | `GET /api/v1/open-api/authentication/verifyAuth` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Base Scenario Plan](actions/create-base-scenario-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Daily Plan](actions/create-daily-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Daily Plans In Bulk](actions/create-daily-plans-in-bulk.md) | `POST /api/v1/open-api/plans/bulk` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Invoice](actions/create-invoice.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Monthly Plan](actions/create-monthly-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Monthly Plans In Bulk](actions/create-monthly-plans-in-bulk.md) | `POST /api/v1/open-api/plans/bulk` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Plan](actions/create-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Plans In Bulk](actions/create-plans-in-bulk.md) | `POST /api/v1/open-api/plans/bulk` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Purchase Credit Note](actions/create-purchase-credit-note.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Purchase Invoice](actions/create-purchase-invoice.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Sales Credit Note](actions/create-sales-credit-note.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Sales Invoice](actions/create-sales-invoice.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Scenario Plan](actions/create-scenario-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Weekly Plan](actions/create-weekly-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Create Weekly Plans In Bulk](actions/create-weekly-plans-in-bulk.md) | `POST /api/v1/open-api/plans/bulk` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Delete Category Plans In Scenario](actions/delete-category-plans-in-scenario.md) | `DELETE /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Delete Invoice](actions/delete-invoice.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Delete Plans](actions/delete-plans.md) | `DELETE /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Get Scenario](actions/get-scenario.md) | `GET /api/v1/open-api/scenarios/:scenarioId` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [List Base Scenarios](actions/list-base-scenarios.md) | `GET /api/v1/open-api/scenarios` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [List Categories](actions/list-categories.md) | `GET /api/v1/open-api/categories` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [List Categories For Planned Transactions](actions/list-categories-for-planned-transactions.md) | `GET /api/v1/open-api/categories` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [List Expense Categories](actions/list-expense-categories.md) | `GET /api/v1/open-api/categories` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [List Income Categories](actions/list-income-categories.md) | `GET /api/v1/open-api/categories` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [List Scenarios](actions/list-scenarios.md) | `GET /api/v1/open-api/scenarios` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Mark Invoice Paid](actions/mark-invoice-paid.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Replace Period Plan](actions/replace-period-plan.md) | `POST /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Reset Scenario Plans For Category](actions/reset-scenario-plans-for-category.md) | `DELETE /api/v1/open-api/plans` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Update Invoice](actions/update-invoice.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
| [Void Invoice](actions/void-invoice.md) | `POST /api/v1/open-api/invoices` | [docs](https://api.tidely.com/tidely-open-api-docs) |
