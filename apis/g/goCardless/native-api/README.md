# GoCardless: Native API Reference

A consolidated summary of GoCardless's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://developer.gocardless.com/api-reference/
- **API base URL:** `https://api-sandbox.gocardless.com`

## Authentication

### API Key

### Credentials

- **Access token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.gocardless.com/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `meta.cursors.after`.

## Pagination

Use `limit` in the query string to set the page size. Use `after` in the query string as the pagination cursor.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Billing Request](actions/cancel-billing-request.md) | `POST /billing_requests/:billingRequestId/actions/cancel` | [docs](https://developer.gocardless.com/api-reference/#billing-requests-cancel-a-billing-request) |
| [Cancel Mandate](actions/cancel-mandate.md) | `POST /mandates/:identity/actions/cancel` | [docs](https://developer.gocardless.com/api-reference/#mandates-cancel-a-mandate) |
| [Cancel Payment](actions/cancel-payment.md) | `POST /payments/:identity/actions/cancel` | [docs](https://developer.gocardless.com/api-reference/#payments-cancel-a-payment) |
| [Collect Billing Request Customer Details](actions/collect-billing-request-customer-details.md) | `POST /billing_requests/:billingRequestId/actions/collect_customer_details` | [docs](https://developer.gocardless.com/api-reference/#billing-requests-collect-customer-details) |
| [Create Billing Request](actions/create-billing-request.md) | `POST /billing_requests` | [docs](https://developer.gocardless.com/api-reference/#billing-requests-create-a-billing-request) |
| [Create Billing Request Flow](actions/create-billing-request-flow.md) | `POST /billing_request_flows` | [docs](https://developer.gocardless.com/api-reference/#billing-request-flows-create-a-billing-request-flow) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://developer.gocardless.com/api-reference/#customers-create-a-customer) |
| [Create Customer Bank Account](actions/create-customer-bank-account.md) | `POST /customer_bank_accounts` | [docs](https://developer.gocardless.com/api-reference/#customer-bank-accounts-create-a-customer-bank-account) |
| [Create Mandate](actions/create-mandate.md) | `POST /mandates` | [docs](https://developer.gocardless.com/api-reference/#mandates-create-a-mandate) |
| [Create Payment](actions/create-payment.md) | `POST /payments` | [docs](https://developer.gocardless.com/api-reference/#payments-create-a-payment) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://developer.gocardless.com/api-reference/#subscriptions-create-a-subscription) |
| [Get Billing Request](actions/get-billing-request.md) | `GET /billing_requests/:billingRequestId` | [docs](https://developer.gocardless.com/api-reference/#billing-requests-get-a-single-billing-request) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerId` | [docs](https://developer.gocardless.com/api-reference/#customers-get-a-single-customer) |
| [Get Event](actions/get-event.md) | `GET /events/:identity` | [docs](https://developer.gocardless.com/api-reference/#events-get-a-single-event) |
| [Get Mandate](actions/get-mandate.md) | `GET /mandates/:identity` | [docs](https://developer.gocardless.com/api-reference/#mandates-get-a-single-mandate) |
| [Get Payment](actions/get-payment.md) | `GET /payments/:identity` | [docs](https://developer.gocardless.com/api-reference/#payments-get-a-single-payment) |
| [Initialise Billing Request Flow](actions/initialise-billing-request-flow.md) | `POST /billing_request_flows/:billingRequestFlowId/actions/initialise` | [docs](https://developer.gocardless.com/api-reference/#billing-request-flows-initialise-a-billing-request-flow) |
| [List Billing Requests](actions/list-billing-requests.md) | `GET /billing_requests` | [docs](https://developer.gocardless.com/api-reference/#billing-requests-list-billing-requests) |
| [List Creditors](actions/list-creditors.md) | `GET /creditors` | [docs](https://developer.gocardless.com/api-reference/#creditors-list-creditors) |
| [List Customer Bank Accounts](actions/list-customer-bank-accounts.md) | `GET /customer_bank_accounts` | [docs](https://developer.gocardless.com/api-reference/#customer-bank-accounts-list-customer-bank-accounts) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developer.gocardless.com/api-reference/#customers-list-customers) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developer.gocardless.com/api-reference/#events-list-events) |
| [List Mandates](actions/list-mandates.md) | `GET /mandates` | [docs](https://developer.gocardless.com/api-reference/#mandates-list-mandates) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://developer.gocardless.com/api-reference/#payments-list-payments) |
| [List Refunds](actions/list-refunds.md) | `GET /refunds` | [docs](https://developer.gocardless.com/api-reference/#refunds-list-refunds) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://developer.gocardless.com/api-reference/#subscriptions-list-subscriptions) |
| [Retry Payment](actions/retry-payment.md) | `POST /payments/:identity/actions/retry` | [docs](https://developer.gocardless.com/api-reference/#payments-retry-a-payment) |
