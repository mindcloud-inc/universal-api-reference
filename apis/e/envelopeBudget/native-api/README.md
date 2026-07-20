# EnvelopeBudget: Native API Reference

A consolidated summary of EnvelopeBudget's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://envelopebudget.com/api/docs
- **OpenAPI specification:** https://envelopebudget.com/api/openapi.json
- **API base URL:** `https://envelopebudget.com/api`

## Authentication

### API Key

Use an EnvelopeBudget API key to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://envelopebudget.com/integrations/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [Create Category](actions/create-category.md) | `POST /categories/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [Create Transaction](actions/create-transaction.md) | `POST /transactions/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [Delete Account](actions/delete-account.md) | `POST /accounts/:budget_id/delete/:account_id` | [docs](https://envelopebudget.com/api/docs) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:budget_id/:category_id` | [docs](https://envelopebudget.com/api/docs) |
| [Delete Envelope](actions/delete-envelope.md) | `DELETE /envelopes/:budget_id/:envelope_id` | [docs](https://envelopebudget.com/api/docs) |
| [Delete Transaction](actions/delete-transaction.md) | `DELETE /transactions/:budget_id/:transaction_id` | [docs](https://envelopebudget.com/api/docs) |
| [Get Account](actions/get-account.md) | `GET /accounts/:budget_id/:account_id` | [docs](https://envelopebudget.com/api/docs) |
| [Get Budget](actions/get-budget.md) | `GET /budgets/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [Get Category](actions/get-category.md) | `GET /categories/:budget_id/:category_id` | [docs](https://envelopebudget.com/api/docs) |
| [Get Envelope](actions/get-envelope.md) | `GET /envelopes/:budget_id/:envelope_id` | [docs](https://envelopebudget.com/api/docs) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:budget_id/:transaction_id` | [docs](https://envelopebudget.com/api/docs) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [List Budgets](actions/list-budgets.md) | `GET /budgets` | [docs](https://envelopebudget.com/api/docs) |
| [List Categories](actions/list-categories.md) | `GET /categories/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [List Envelopes](actions/list-envelopes.md) | `GET /envelopes/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions/:budget_id` | [docs](https://envelopebudget.com/api/docs) |
| [Patch Transaction](actions/patch-transaction.md) | `PATCH /transactions/:budget_id/:transaction_id` | [docs](https://envelopebudget.com/api/docs) |
| [Update Account](actions/update-account.md) | `PUT /accounts/:budget_id/:account_id` | [docs](https://envelopebudget.com/api/docs) |
| [Update Category](actions/update-category.md) | `PATCH /categories/:budget_id/:category_id` | [docs](https://envelopebudget.com/api/docs) |
| [Update Envelope](actions/update-envelope.md) | `PATCH /envelopes/:budget_id/:envelope_id` | [docs](https://envelopebudget.com/api/docs) |
