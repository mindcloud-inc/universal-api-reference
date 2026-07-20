# Recurly: Native API Reference

A consolidated summary of Recurly's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://recurly.com/developers/api/
- **OpenAPI specification:** https://raw.githubusercontent.com/recurly/recurly-client-go/v3-v2021-02-25/openapi/api.yaml
- **API base URL:** `https://v3.recurly.com`

## Authentication

### API Key

Use your Recurly private API key. The wrapper sends it with Recurly's Basic-auth header format.

### Credentials

- **API Key:** `apiKey` · required
- **API Base URL:** `apiBaseUrl` · required · Use https://v3.recurly.com for US sites or https://v3.eu.recurly.com for EU sites.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.recurly.com/recurly-subscriptions/docs/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.recurly.v2021-02-25` |
| `Content-Type` | `application/json` |

The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–200).

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `PUT /subscriptions/:subscription_id/cancel` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/cancel_subscription) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/create_account) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/create_subscription) |
| [Deactivate Account](actions/deactivate-account.md) | `DELETE /accounts/:account_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/deactivate_account) |
| [Fetch Account](actions/fetch-account.md) | `GET /accounts/:account_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_account) |
| [Fetch Account Balance](actions/fetch-account-balance.md) | `GET /accounts/:account_id/balance` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_account_balance) |
| [Fetch Invoice](actions/fetch-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_invoice) |
| [Fetch Plan](actions/fetch-plan.md) | `GET /plans/:plan_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_plan) |
| [Fetch Preview Renewal](actions/fetch-preview-renewal.md) | `GET /subscriptions/:subscription_id/preview_renewal` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_preview_renewal) |
| [Fetch Subscription](actions/fetch-subscription.md) | `GET /subscriptions/:subscription_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_subscription) |
| [Fetch Transaction](actions/fetch-transaction.md) | `GET /transactions/:transaction_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/get_transaction) |
| [List Account Subscriptions](actions/list-account-subscriptions.md) | `GET /accounts/:account_id/subscriptions` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_account_subscriptions) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_accounts) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_invoices) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_plans) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_sites) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_subscriptions) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/list_transactions) |
| [Pause Subscription](actions/pause-subscription.md) | `PUT /subscriptions/:subscription_id/pause` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/pause_subscription) |
| [Reactivate Account](actions/reactivate-account.md) | `PUT /accounts/:account_id/reactivate` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/reactivate_account) |
| [Reactivate Subscription](actions/reactivate-subscription.md) | `PUT /subscriptions/:subscription_id/reactivate` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/reactivate_subscription) |
| [Update Account](actions/update-account.md) | `PUT /accounts/:account_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/update_account) |
| [Update Subscription](actions/update-subscription.md) | `PUT /subscriptions/:subscription_id` | [docs](https://recurly.com/developers/api/v2021-02-25/#operation/update_subscription) |
