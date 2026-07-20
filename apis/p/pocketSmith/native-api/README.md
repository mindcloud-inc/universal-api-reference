# PocketSmith: Native API Reference

A consolidated summary of PocketSmith's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.pocketsmith.com/docs/introduction
- **API base URL:** `https://api.pocketsmith.com/v2`

## Authentication

### PocketSmith API Key

Use a PocketSmith developer key for the PocketSmith account you want to connect.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Developer-Key: <apiKey>
```

[Official authentication documentation](https://learn.pocketsmith.com/article/1538-pocketsmith-api-developer-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Category In User](actions/create-category-in-user.md) | `POST /users/:id/categories` | [docs](https://developers.pocketsmith.com/reference/post_users-id-categories-1) |
| [Create Category Rule In Category](actions/create-category-rule-in-category.md) | `POST /categories/:id/category_rules` | [docs](https://developers.pocketsmith.com/reference/post_categories-id-category-rules-1) |
| [Create Institution In User](actions/create-institution-in-user.md) | `POST /users/:id/institutions` | [docs](https://developers.pocketsmith.com/reference/post_users-id-institutions-1) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:id` | [docs](https://developers.pocketsmith.com/reference/delete_categories-id-1) |
| [Delete Forecast Cache For User](actions/delete-forecast-cache-for-user.md) | `DELETE /users/:id/forecast_cache` | [docs](https://developers.pocketsmith.com/reference/delete_users-id-forecast-cache) |
| [Delete Institution](actions/delete-institution.md) | `DELETE /institutions/:id` | [docs](https://developers.pocketsmith.com/reference/delete_institutions-id-1) |
| [Get Authorised User](actions/get-authorised-user.md) | `GET /me` | [docs](https://developers.pocketsmith.com/reference/get_me-1) |
| [Get Budget Summary For User](actions/get-budget-summary-for-user.md) | `GET /users/:id/budget_summary` | [docs](https://developers.pocketsmith.com/reference/get_users-id-budget-summary-1) |
| [Get Category](actions/get-category.md) | `GET /categories/:id` | [docs](https://developers.pocketsmith.com/reference/get_categories-id-1) |
| [Get Currency](actions/get-currency.md) | `GET /currencies/:id` | [docs](https://developers.pocketsmith.com/reference/get_currencies-id) |
| [Get Institution](actions/get-institution.md) | `GET /institutions/:id` | [docs](https://developers.pocketsmith.com/reference/get_institutions-id-1) |
| [Get Trend Analysis For User](actions/get-trend-analysis-for-user.md) | `GET /users/:id/trend_analysis` | [docs](https://developers.pocketsmith.com/reference/get_users-id-trend-analysis-1) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.pocketsmith.com/reference/get_users-id-1) |
| [List Accounts In User](actions/list-accounts-in-user.md) | `GET /users/:id/accounts` | [docs](https://developers.pocketsmith.com/reference/get_users-id-accounts-1) |
| [List Budget For User](actions/list-budget-for-user.md) | `GET /users/:id/budget` | [docs](https://developers.pocketsmith.com/reference/get_users-id-budget-1) |
| [List Categories In User](actions/list-categories-in-user.md) | `GET /users/:id/categories` | [docs](https://developers.pocketsmith.com/reference/get_users-id-categories-1) |
| [List Category Rules In User](actions/list-category-rules-in-user.md) | `GET /users/:id/category_rules` | [docs](https://developers.pocketsmith.com/reference/get_users-id-category-rules-1) |
| [List Currencies](actions/list-currencies.md) | `GET /currencies` | [docs](https://developers.pocketsmith.com/reference/get_currencies) |
| [List Institutions In User](actions/list-institutions-in-user.md) | `GET /users/:id/institutions` | [docs](https://developers.pocketsmith.com/reference/get_users-id-institutions-1) |
| [List Transaction Accounts In User](actions/list-transaction-accounts-in-user.md) | `GET /users/:id/transaction_accounts` | [docs](https://developers.pocketsmith.com/reference/get_users-id-transaction-accounts-1) |
| [List Transactions In Categories](actions/list-transactions-in-categories.md) | `GET /categories/:id/transactions` | [docs](https://developers.pocketsmith.com/reference/get_categories-id-transactions) |
| [List Transactions In User](actions/list-transactions-in-user.md) | `GET /users/:id/transactions` | [docs](https://developers.pocketsmith.com/reference/get_users-id-transactions-1) |
| [Update Category](actions/update-category.md) | `PUT /categories/:id` | [docs](https://developers.pocketsmith.com/reference/put_categories-id-1) |
| [Update Institution](actions/update-institution.md) | `PUT /institutions/:id` | [docs](https://developers.pocketsmith.com/reference/put_institutions-id-1) |
