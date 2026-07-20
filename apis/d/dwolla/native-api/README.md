# Dwolla: Native API Reference

A consolidated summary of Dwolla's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.dwolla.com/docs/api-reference/root
- **API base URL:** `https://api-sandbox.dwolla.com`

## Authentication

### OAuth 2.0 (Client Credentials)

Use Dwolla client credentials to obtain an application access token for server-to-server API access.

### Credentials

- **Client ID:** `clientId` · optional · Dwolla sandbox application client ID.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api-sandbox.dwolla.com/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.dwolla.com/docs/connect/api-reference/api-fundamentals/making-requests-and-authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.dwolla.v1.hal+json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Transfer](actions/cancel-transfer.md) | `POST /transfers/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/transfers/cancel-a-transfer) |
| [Create Account Funding Source](actions/create-account-funding-source.md) | `POST /funding-sources` | [docs](https://developers.dwolla.com/docs/api-reference/accounts/create-a-funding-source-for-an-account) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://developers.dwolla.com/docs/api-reference/customers/create-a-customer) |
| [Create Customer Funding Source](actions/create-customer-funding-source.md) | `POST /customers/[:id]/funding-sources` | [docs](https://developers.dwolla.com/docs/api-reference/funding-sources/create-customer-funding-source) |
| [Create Transfer](actions/create-transfer.md) | `POST /transfers` | [docs](https://developers.dwolla.com/docs/api-reference/transfers/initiate-a-transfer) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhook-subscriptions` | [docs](https://developers.dwolla.com/docs/api-reference/webhook-subscriptions/create-a-webhook-subscription) |
| [Get Account](actions/get-account.md) | `GET /accounts/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/accounts/retrieve-account-details) |
| [Get Business Classification](actions/get-business-classification.md) | `GET /business-classifications/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/customers/retrieve-a-business-classification) |
| [Get Customer](actions/get-customer.md) | `GET /customers/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/customers/retrieve-a-customer) |
| [Get Funding Source](actions/get-funding-source.md) | `GET /funding-sources/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/funding-sources/retrieve-a-funding-source) |
| [Get Funding Source Balance](actions/get-funding-source-balance.md) | `GET /funding-sources/[:id]/balance` | [docs](https://developers.dwolla.com/docs/api-reference/funding-sources/retrieve-funding-source-balance) |
| [Get Root](actions/get-root.md) | `GET /` | [docs](https://developers.dwolla.com/docs/api-reference/root) |
| [Get Transfer](actions/get-transfer.md) | `GET /transfers/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/transfers/retrieve-a-transfer) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /webhook-subscriptions/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/webhook-subscriptions/retrieve-a-webhook-subscription) |
| [List Account Funding Sources](actions/list-account-funding-sources.md) | `GET /accounts/[:id]/funding-sources` | [docs](https://developers.dwolla.com/docs/api-reference/accounts/list-funding-sources-for-an-account) |
| [List Account Transfers](actions/list-account-transfers.md) | `GET /accounts/[:id]/transfers` | [docs](https://developers.dwolla.com/docs/api-reference/accounts/list-and-search-transfers-for-an-account) |
| [List Business Classifications](actions/list-business-classifications.md) | `GET /business-classifications` | [docs](https://developers.dwolla.com/docs/api-reference/customers/list-business-classifications) |
| [List Customer Funding Sources](actions/list-customer-funding-sources.md) | `GET /customers/[:id]/funding-sources` | [docs](https://developers.dwolla.com/docs/api-reference/funding-sources/list-customer-funding-sources) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developers.dwolla.com/docs/api-reference/customers/list-and-search-customers) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developers.dwolla.com/docs/api-reference/events/list-events) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhook-subscriptions` | [docs](https://developers.dwolla.com/docs/api-reference/webhook-subscriptions/list-webhook-subscriptions) |
| [Remove Funding Source](actions/remove-funding-source.md) | `POST /funding-sources/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/funding-sources/update-or-remove-a-funding-source) |
| [Update Customer](actions/update-customer.md) | `POST /customers/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/customers/update-a-customer) |
| [Update Funding Source](actions/update-funding-source.md) | `POST /funding-sources/[:id]` | [docs](https://developers.dwolla.com/docs/api-reference/funding-sources/update-or-remove-a-funding-source) |
