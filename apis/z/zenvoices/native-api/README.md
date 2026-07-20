# Zenvoices: Native API Reference

A consolidated summary of Zenvoices's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.zenvoices.com/blog/public-api-docs/
- **OpenAPI specification:** https://app.zenvoices.com/swagger/public-v1/swagger.json
- **API base URL:** `https://app.zenvoices.com`

## Authentication

### Username and password

Authenticate to Zenvoices with a username or email address, password, and optional tenancy name. The authentication action calls Zenvoices TokenLogin and stores the returned bearer access token.

### Credentials

- **Username or email address:** `userNameOrEmailAddress` · required · Zenvoices login username or email address.
- **Tenancy name:** `tenancyName` · optional · Optional Zenvoices tenant name. Use mindcloud for the MindCloud sandbox tenant.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://app.zenvoices.com/swagger/public-v1/swagger.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `maxResultCount` in the request body to set the page size (default 50; accepted range 1–250). Use `skipCount` in the request body as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sorting` in the request body. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account By Code](actions/get-account-by-code.md) | `GET /public-api/v1/accounts` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Account By External ID](actions/get-account-by-external-id.md) | `GET /public-api/v1/accounts/externalId` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Administration](actions/get-administration.md) | `GET /public-api/v1/administration/{administrationId}` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Employee By Code](actions/get-employee-by-code.md) | `GET /public-api/v1/employees` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Financial Transaction](actions/get-financial-transaction.md) | `GET /public-api/v1/financialTransaction/{financialTransactionId}` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Inbox Document](actions/get-inbox-document.md) | `GET /public-api/v1/inbox/details` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Ledger Account By Code](actions/get-ledger-account-by-code.md) | `GET /public-api/v1/ledgerAccounts` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Product By Code](actions/get-product-by-code.md) | `GET /public-api/v1/product` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Project By Code](actions/get-project-by-code.md) | `GET /public-api/v1/projects` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /public-api/v1/purchaseOrders` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Accounts](actions/list-accounts.md) | `POST /public-api/v1/accounts/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Administrations](actions/list-administrations.md) | `POST /public-api/v1/administration/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Available Webhooks](actions/list-available-webhooks.md) | `GET /public-api/v1/webhookSubscription/get-available-webhooks` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Cost Centres](actions/list-cost-centres.md) | `POST /public-api/v1/costCentres/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Cost Units](actions/list-cost-units.md) | `POST /public-api/v1/costUnits/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Employees](actions/list-employees.md) | `POST /public-api/v1/employees/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Financial Transactions](actions/list-financial-transactions.md) | `POST /public-api/v1/financialTransaction/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Inbox Documents](actions/list-inbox-documents.md) | `POST /public-api/v1/inbox/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | `POST /public-api/v1/ledgerAccounts/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Payment Conditions](actions/list-payment-conditions.md) | `POST /public-api/v1/paymentConditions/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Products](actions/list-products.md) | `POST /public-api/v1/product/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Projects](actions/list-projects.md) | `POST /public-api/v1/projects/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST /public-api/v1/purchaseOrders/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Tax Codes](actions/list-tax-codes.md) | `POST /public-api/v1/taxCodes/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /public-api/v1/webhookSubscription/list` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
| [Token Login](actions/token-login.md) | `POST /api/TokenAuth/TokenLogin` | [docs](https://app.zenvoices.com/swagger/public-v1/swagger.json) |
