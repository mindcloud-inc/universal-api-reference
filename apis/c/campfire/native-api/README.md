# Campfire: Native API Reference

A consolidated summary of Campfire's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.campfire.ai/
- **OpenAPI specification:** https://api.meetcampfire.com/api/schema?format=json
- **API base URL:** `https://api.meetcampfire.com`

## Authentication

### API Key

Use a Campfire API key in the Authorization header as Token <api-key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.campfire.ai/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | `GET /users/api/get_user_info` | [docs](https://docs.campfire.ai/) |
| [List Accounting Bills](actions/list-accounting-bills.md) | `GET /coa/api/v1/bill/` | [docs](https://docs.campfire.ai/api-reference/accounts-payable/list-accounting-bills) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /ca/api/account` | [docs](https://docs.campfire.ai/api-reference/cash-management/list-bank-accounts) |
| [List Bank Transactions](actions/list-bank-transactions.md) | `GET /ca/api/transaction` | [docs](https://docs.campfire.ai/api-reference/cash-management/list-bank-transactions) |
| [List Budgets](actions/list-budgets.md) | `GET /coa/api/budgets` | [docs](https://docs.campfire.ai/api-reference/core-accounting/list-budgets) |
| [List Chart Entities](actions/list-chart-entities.md) | `GET /coa/api/entity` | [docs](https://docs.campfire.ai/api-reference/settings/list-chart-entities) |
| [List Chart Transactions](actions/list-chart-transactions.md) | `GET /coa/api/transaction` | [docs](https://docs.campfire.ai/api-reference/core-accounting/list-chart-transactions) |
| [List Credit Memos](actions/list-credit-memos.md) | `GET /coa/api/v1/credit-memo` | [docs](https://docs.campfire.ai/api-reference/accounts-receivable/list-credit-memos) |
| [List Departments](actions/list-departments.md) | `GET /coa/api/department` | [docs](https://docs.campfire.ai/api-reference/company-objects/list-departments) |
| [List Entity Access](actions/list-entity-access.md) | `GET /users/api/entity-access/` | [docs](https://docs.campfire.ai/) |
| [List Fixed Assets](actions/list-fixed-assets.md) | `GET /coa/api/fixed-asset` | [docs](https://docs.campfire.ai/api-reference/core-accounting/list-fixed-assets) |
| [List Invoices](actions/list-invoices.md) | `GET /coa/api/v1/invoice/` | [docs](https://docs.campfire.ai/api-reference/accounts-receivable/list-invoices) |
| [List Journal Entries](actions/list-journal-entries.md) | `GET /coa/api/journal_entry` | [docs](https://docs.campfire.ai/api-reference/core-accounting/list-journal-entries) |
| [List Vendors](actions/list-vendors.md) | `GET /coa/api/vendor` | [docs](https://docs.campfire.ai/api-reference/company-objects/list-vendors) |
| [Retrieve Accounting Bill](actions/retrieve-accounting-bill.md) | `GET /coa/api/v1/bill/:id/` | [docs](https://docs.campfire.ai/api-reference/accounts-payable/retrieve-accounting-bill) |
| [Retrieve Bank Account](actions/retrieve-bank-account.md) | `GET /ca/api/account/:id` | [docs](https://docs.campfire.ai/api-reference/cash-management/retrieve-bank-account) |
| [Retrieve Bank Transaction](actions/retrieve-bank-transaction.md) | `GET /ca/api/transaction/:id` | [docs](https://docs.campfire.ai/api-reference/cash-management/retrieve-bank-transaction) |
| [Retrieve Budget](actions/retrieve-budget.md) | `GET /coa/api/budgets/:id` | [docs](https://docs.campfire.ai/api-reference/core-accounting/retrieve-budget) |
| [Retrieve Chart Entity](actions/retrieve-chart-entity.md) | `GET /coa/api/entity/:id` | [docs](https://docs.campfire.ai/api-reference/settings/retrieve-chart-entity) |
| [Retrieve Chart Transaction](actions/retrieve-chart-transaction.md) | `GET /coa/api/transaction/:id` | [docs](https://docs.campfire.ai/api-reference/core-accounting/retrieve-chart-transaction) |
| [Retrieve Credit Memo](actions/retrieve-credit-memo.md) | `GET /coa/api/v1/credit-memo/:id` | [docs](https://docs.campfire.ai/api-reference/accounts-receivable/retrieve-credit-memo) |
| [Retrieve Department](actions/retrieve-department.md) | `GET /coa/api/department/:id` | [docs](https://docs.campfire.ai/api-reference/company-objects/retrieve-department) |
| [Retrieve Fixed Asset](actions/retrieve-fixed-asset.md) | `GET /coa/api/fixed-asset/:id` | [docs](https://docs.campfire.ai/api-reference/core-accounting/retrieve-fixed-asset) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /coa/api/v1/invoice/:id/` | [docs](https://docs.campfire.ai/api-reference/accounts-receivable/retrieve-invoice) |
| [Retrieve Journal Entry](actions/retrieve-journal-entry.md) | `GET /coa/api/journal_entry/:id` | [docs](https://docs.campfire.ai/api-reference/core-accounting/retrieve-journal-entry) |
| [Retrieve Vendor](actions/retrieve-vendor.md) | `GET /coa/api/vendor/:id` | [docs](https://docs.campfire.ai/api-reference/company-objects/retrieve-vendor) |
