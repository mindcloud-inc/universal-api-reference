# VentiPay: Native API Reference

A consolidated summary of VentiPay's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.ventipay.com/docs/welcome
- **API base URL:** `https://api.ventipay.com/v1`

## Authentication

### Secret API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ventipay.com/reference/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–200).

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.ventipay.com/reference/customers-create) |
| [Get Balance](actions/get-balance.md) | `GET /balance` | [docs](https://docs.ventipay.com/reference/balance-get) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://docs.ventipay.com/reference/customers-get) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.ventipay.com/reference/customers-list) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://docs.ventipay.com/reference/invoices-list) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /payment_methods` | [docs](https://docs.ventipay.com/reference/payment_methods-list) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://docs.ventipay.com/reference/payments-list) |
| [List Payouts](actions/list-payouts.md) | `GET /payouts` | [docs](https://docs.ventipay.com/reference/payouts-list) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://docs.ventipay.com/reference/plans-list) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://docs.ventipay.com/reference/subscriptions-list) |
