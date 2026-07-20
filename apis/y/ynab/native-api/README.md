# YNAB: Native API Reference

A consolidated summary of YNAB's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://api.ynab.com
- **OpenAPI specification:** https://api.ynab.com/papi/open_api_spec.yaml
- **API base URL:** `https://api.ynab.com/v1`

## Authentication

### Personal Access Token

Use a YNAB personal access token for your own account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.ynab.com/#personal-access-tokens)

### OAuth 2.0

Connect YNAB with OAuth for multi-user or shareable integrations.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.ynab.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.ynab.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.ynab.com/oauth/token.

[Official authentication documentation](https://api.ynab.com/#oauth-applications)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /plans/:planId/accounts/:accountId` | [docs](https://api.ynab.com/v1) |
| [Get Category](actions/get-category.md) | `GET /plans/:planId/categories/:categoryId` | [docs](https://api.ynab.com/v1) |
| [Get Month](actions/get-month.md) | `GET /plans/:planId/months/:month` | [docs](https://api.ynab.com/v1) |
| [Get Month Category](actions/get-month-category.md) | `GET /plans/:planId/months/:month/categories/:categoryId` | [docs](https://api.ynab.com/v1) |
| [Get Payee](actions/get-payee.md) | `GET /plans/:planId/payees/:payeeId` | [docs](https://api.ynab.com/v1) |
| [Get Payee Location](actions/get-payee-location.md) | `GET /plans/:planId/payee_locations/:payeeLocationId` | [docs](https://api.ynab.com/v1) |
| [Get Plan](actions/get-plan.md) | `GET /plans/:planId` | [docs](https://api.ynab.com/v1) |
| [Get Plan Settings](actions/get-plan-settings.md) | `GET /plans/:planId/settings` | [docs](https://api.ynab.com/v1) |
| [Get Scheduled Transaction](actions/get-scheduled-transaction.md) | `GET /plans/:planId/scheduled_transactions/:scheduledTransactionId` | [docs](https://api.ynab.com/v1) |
| [Get Transaction](actions/get-transaction.md) | `GET /plans/:planId/transactions/:transactionId` | [docs](https://api.ynab.com/v1) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://api.ynab.com/v1) |
| [List Account Transactions](actions/list-account-transactions.md) | `GET /plans/:planId/accounts/:accountId/transactions` | [docs](https://api.ynab.com/v1) |
| [List Accounts](actions/list-accounts.md) | `GET /plans/:planId/accounts` | [docs](https://api.ynab.com/v1) |
| [List Categories](actions/list-categories.md) | `GET /plans/:planId/categories` | [docs](https://api.ynab.com/v1) |
| [List Category Transactions](actions/list-category-transactions.md) | `GET /plans/:planId/categories/:categoryId/transactions` | [docs](https://api.ynab.com/v1) |
| [List Money Movement Groups](actions/list-money-movement-groups.md) | `GET /plans/:planId/money_movement_groups` | [docs](https://api.ynab.com/v1) |
| [List Money Movements](actions/list-money-movements.md) | `GET /plans/:planId/money_movements` | [docs](https://api.ynab.com/v1) |
| [List Month Money Movement Groups](actions/list-month-money-movement-groups.md) | `GET /plans/:planId/months/:month/money_movement_groups` | [docs](https://api.ynab.com/v1) |
| [List Month Money Movements](actions/list-month-money-movements.md) | `GET /plans/:planId/months/:month/money_movements` | [docs](https://api.ynab.com/v1) |
| [List Month Transactions](actions/list-month-transactions.md) | `GET /plans/:planId/months/:month/transactions` | [docs](https://api.ynab.com/v1) |
| [List Months](actions/list-months.md) | `GET /plans/:planId/months` | [docs](https://api.ynab.com/v1) |
| [List Payee Locations](actions/list-payee-locations.md) | `GET /plans/:planId/payee_locations` | [docs](https://api.ynab.com/v1) |
| [List Payee Locations For Payee](actions/list-payee-locations-for-payee.md) | `GET /plans/:planId/payees/:payeeId/payee_locations` | [docs](https://api.ynab.com/v1) |
| [List Payee Transactions](actions/list-payee-transactions.md) | `GET /plans/:planId/payees/:payeeId/transactions` | [docs](https://api.ynab.com/v1) |
| [List Payees](actions/list-payees.md) | `GET /plans/:planId/payees` | [docs](https://api.ynab.com/v1) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://api.ynab.com/v1) |
| [List Scheduled Transactions](actions/list-scheduled-transactions.md) | `GET /plans/:planId/scheduled_transactions` | [docs](https://api.ynab.com/v1) |
| [List Transactions](actions/list-transactions.md) | `GET /plans/:planId/transactions` | [docs](https://api.ynab.com/v1) |
