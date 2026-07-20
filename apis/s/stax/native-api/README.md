# Stax: Native API Reference

A consolidated summary of Stax's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://docs.staxpayments.com/reference
- **API base URL:** `https://apiprod.fattlabs.com`

## Authentication

### API Key

Use a Stax merchant API key for server-side API access. MindCloud will send it as `Authorization: Bearer {{credentials.apiKey}}`. The hosted payments token is separate and is only needed for hosted/web payments flows.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.staxpayments.com/reference/merchant-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Pre-Auth Transaction](actions/capture-pre-auth-transaction.md) | `POST /transaction/:transactionid/capture` | [docs](https://docs.staxpayments.com/reference/capture-a-pre-auth-transaction) |
| [Charge Payment Method](actions/charge-payment-method.md) | `POST /charge` | [docs](https://docs.staxpayments.com/reference/charge-a-payment-method) |
| [Create Card Payment Method](actions/create-card-payment-method.md) | `POST /payment-method/` | [docs](https://docs.staxpayments.com/reference/create-a-payment-method) |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://docs.staxpayments.com/reference/create-customer) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /query/payment-links` | [docs](https://docs.staxpayments.com/reference/create-a-payment-link) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customer/:id` | [docs](https://docs.staxpayments.com/reference/delete-a-customer) |
| [Delete Payment Link](actions/delete-payment-link.md) | `DELETE /query/payment-links/:id` | [docs](https://docs.staxpayments.com/reference/delete-a-payment-link) |
| [Delete Payment Method](actions/delete-payment-method.md) | `DELETE /payment-method/:id` | [docs](https://docs.staxpayments.com/reference/delete-a-payment-method) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:id` | [docs](https://docs.staxpayments.com/reference/get-a-customers-information) |
| [Get Daily Sales](actions/get-daily-sales.md) | `GET /query/statement/v3/daily-sales` | [docs](https://docs.staxpayments.com/reference/daily-sales) |
| [Get Deposit Details](actions/get-deposit-details.md) | `GET /query/depositDetail` | [docs](https://docs.staxpayments.com/reference/get-details-of-specific-deposit) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoice/:id` | [docs](https://docs.staxpayments.com/reference/get-an-invoice) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /query/payment-links/:id` | [docs](https://docs.staxpayments.com/reference/get-a-payment-links-information) |
| [Get Payment Link Active Status](actions/get-payment-link-active-status.md) | `GET /query/payment-links/:id/is-active` | [docs](https://docs.staxpayments.com/reference/get-a-payment-links-active-status) |
| [Get Payment Method](actions/get-payment-method.md) | `GET /payment-method/:id` | [docs](https://docs.staxpayments.com/reference/get-a-payment-method-by-id) |
| [Get Related Transactions](actions/get-related-transactions.md) | `GET /transaction/:id/related` | [docs](https://docs.staxpayments.com/reference/get-a-related-transaction) |
| [Get Statement ACH Rejections](actions/get-statement-ach-rejections.md) | `GET /query/statement/v3/ach-rejects` | [docs](https://docs.staxpayments.com/reference/ach-rejections) |
| [Get Statement Card Processing](actions/get-statement-card-processing.md) | `GET /query/statement/v3/volumes/card-processing` | [docs](https://docs.staxpayments.com/reference/card-processing) |
| [Get Statement Disputes](actions/get-statement-disputes.md) | `GET /query/statement/v3/disputes` | [docs](https://docs.staxpayments.com/reference/disputes) |
| [Get Statement Fees](actions/get-statement-fees.md) | `GET /query/statement/v3/fees` | [docs](https://docs.staxpayments.com/reference/get-statement-information) |
| [Get Statement Refunds and Adjustments](actions/get-statement-refunds-and-adjustments.md) | `GET /query/statement/v3/adjustments` | [docs](https://docs.staxpayments.com/reference/refund-and-adjustments) |
| [Get Statement Surcharging](actions/get-statement-surcharging.md) | `GET /query/statement/v3/surcharges` | [docs](https://docs.staxpayments.com/reference/surcharging-1) |
| [Get Statement Volumes by Card Type](actions/get-statement-volumes-by-card-type.md) | `GET /query/statement/v3/volumes/card-type` | [docs](https://docs.staxpayments.com/reference/volumes-by-card-type) |
| [Get Team Summary](actions/get-team-summary.md) | `GET /query/statistics/teamSummary` | [docs](https://docs.staxpayments.com/docs/performance-analytics) |
| [Get Transaction](actions/get-transaction.md) | `GET /transaction/:id` | [docs](https://docs.staxpayments.com/reference/get-a-transactions-information) |
| [Get Transaction Funding Instructions](actions/get-transaction-funding-instructions.md) | `GET /transaction/:id/funding` | [docs](https://docs.staxpayments.com/reference/get-a-transactions-funding-instructions) |
| [Get User and Team Info](actions/get-user-and-team-info.md) | `GET /self` | [docs](https://docs.staxpayments.com/reference/get-self-and-teams-info) |
| [List Customer Payment Methods](actions/list-customer-payment-methods.md) | `GET /customer/:customerId/payment-method` | [docs](https://docs.staxpayments.com/reference/get-all-payment-methods-for-a-customer) |
| [List Customers](actions/list-customers.md) | `GET /customer` | [docs](https://docs.staxpayments.com/reference/find-all-customers) |
| [List Deposits](actions/list-deposits.md) | `GET /query/deposit` | [docs](https://docs.staxpayments.com/reference/get-list-of-deposits) |
| [List Invoices](actions/list-invoices.md) | `GET /invoice` | [docs](https://docs.staxpayments.com/reference/get-all-invoices) |
| [List Merchant Payment Methods](actions/list-merchant-payment-methods.md) | `GET /payment-method` | [docs](https://docs.staxpayments.com/reference/get-all-payment-methods-for-a-merchant) |
| [List Payment Links](actions/list-payment-links.md) | `GET /query/payment-links` | [docs](https://docs.staxpayments.com/reference/list-and-filter-all-payment-links) |
| [List Team Users](actions/list-team-users.md) | `GET /team/user` | [docs](https://docs.staxpayments.com/reference/find-the-merchant-teams-users) |
| [List Transactions](actions/list-transactions.md) | `GET /transaction` | [docs](https://docs.staxpayments.com/reference/list-and-filter-all-transactions) |
| [Review Transaction Surcharge](actions/review-transaction-surcharge.md) | `GET /surcharge/review` | [docs](https://docs.staxpayments.com/reference/review-a-transactions-surcharge-information) |
| [Update Customer](actions/update-customer.md) | `PUT /customer/:id` | [docs](https://docs.staxpayments.com/reference/update-customer-info) |
| [Update Payment Link](actions/update-payment-link.md) | `PUT /query/payment-links/:id` | [docs](https://docs.staxpayments.com/reference/update-or-deactivate-a-payment-link) |
| [Update Payment Method](actions/update-payment-method.md) | `PUT /payment-method/:id` | [docs](https://docs.staxpayments.com/reference/update-a-payment-method) |
| [Verify Payment Method](actions/verify-payment-method.md) | `POST /verify` | [docs](https://docs.staxpayments.com/reference/verify-a-payment-method) |
| [Void or Refund Transaction](actions/void-or-refund-transaction.md) | `POST /transaction/:id/void-or-refund` | [docs](https://docs.staxpayments.com/reference/void-or-refund-transaction) |
