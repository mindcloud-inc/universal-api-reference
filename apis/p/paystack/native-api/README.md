# Paystack: Native API Reference

A consolidated summary of Paystack's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://paystack.com/docs/api/
- **API base URL:** `https://api.paystack.co`

## Authentication

### Secret Key

Use your Paystack secret key for backend API requests. The public key is optional metadata only.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://paystack.com/docs/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.pageCount`. The current page number is read from `meta.page`.

## Pagination

Use `perPage` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://paystack.com/docs/api/customer/) |
| [Create Page](actions/create-page.md) | `POST /page` | [docs](https://paystack.com/docs/api/page/) |
| [Create Payment Request](actions/create-payment-request.md) | `POST /paymentrequest` | [docs](https://paystack.com/docs/api/payment-request/) |
| [Create Plan](actions/create-plan.md) | `POST /plan` | [docs](https://paystack.com/docs/api/plan/) |
| [Create Product](actions/create-product.md) | `POST /product` | [docs](https://paystack.com/docs/api/product/) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscription` | [docs](https://paystack.com/docs/api/subscription/) |
| [Export Transactions](actions/export-transactions.md) | `GET /transaction/export` | [docs](https://paystack.com/docs/api/transaction/) |
| [Fetch Customer](actions/fetch-customer.md) | `GET /customer/:customerCode` | [docs](https://paystack.com/docs/api/customer/) |
| [Fetch Page](actions/fetch-page.md) | `GET /page/:pageIdOrSlug` | [docs](https://paystack.com/docs/api/page/) |
| [Fetch Payment Request](actions/fetch-payment-request.md) | `GET /paymentrequest/:paymentRequestIdOrCode` | [docs](https://paystack.com/docs/api/payment-request/) |
| [Fetch Plan](actions/fetch-plan.md) | `GET /plan/:planIdOrCode` | [docs](https://paystack.com/docs/api/plan/) |
| [Fetch Product](actions/fetch-product.md) | `GET /product/:productIdOrCode` | [docs](https://paystack.com/docs/api/product/) |
| [Fetch Subscription](actions/fetch-subscription.md) | `GET /subscription/:subscriptionIdOrCode` | [docs](https://paystack.com/docs/api/subscription/) |
| [Fetch Transaction](actions/fetch-transaction.md) | `GET /transaction/:transactionId` | [docs](https://paystack.com/docs/api/transaction/) |
| [Get Transaction Totals](actions/get-transaction-totals.md) | `GET /transaction/totals` | [docs](https://paystack.com/docs/api/transaction/) |
| [Initialize Transaction](actions/initialize-transaction.md) | `POST /transaction/initialize` | [docs](https://paystack.com/docs/api/transaction/) |
| [List Banks](actions/list-banks.md) | `GET /bank` | [docs](https://paystack.com/docs/api/miscellaneous/) |
| [List Countries](actions/list-countries.md) | `GET /country` | [docs](https://paystack.com/docs/api/miscellaneous/) |
| [List Customers](actions/list-customers.md) | `GET /customer` | [docs](https://paystack.com/docs/api/customer/) |
| [List Pages](actions/list-pages.md) | `GET /page` | [docs](https://paystack.com/docs/api/page/) |
| [List Payment Requests](actions/list-payment-requests.md) | `GET /paymentrequest` | [docs](https://paystack.com/docs/api/payment-request/) |
| [List Plans](actions/list-plans.md) | `GET /plan` | [docs](https://paystack.com/docs/api/plan/) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://paystack.com/docs/api/product/) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscription` | [docs](https://paystack.com/docs/api/subscription/) |
| [List Transactions](actions/list-transactions.md) | `GET /transaction` | [docs](https://paystack.com/docs/api/transaction/) |
| [Update Customer](actions/update-customer.md) | `PUT /customer/:customerCode` | [docs](https://paystack.com/docs/api/customer/) |
| [Update Plan](actions/update-plan.md) | `PUT /plan/:planIdOrCode` | [docs](https://paystack.com/docs/api/plan/) |
| [Update Product](actions/update-product.md) | `PUT /product/:productIdOrCode` | [docs](https://paystack.com/docs/api/product/) |
| [Verify Transaction](actions/verify-transaction.md) | `GET /transaction/verify/:reference` | [docs](https://paystack.com/docs/api/transaction/) |
| [Whitelist/Blacklist Customer](actions/whitelist-blacklist-customer.md) | `POST /customer/set_risk_action` | [docs](https://paystack.com/docs/api/customer/) |
