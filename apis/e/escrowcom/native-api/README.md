# Escrow.com: Native API Reference

A consolidated summary of Escrow.com's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.escrow.com/api/docs/basics
- **API base URL:** `https://api.escrow-sandbox.com/2017-09-01`

## Authentication

### Email + API Key

Use your Escrow.com account email as the Basic auth username and an Escrow.com API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.escrow.com/api/docs/basics)

## API conventions

Responses from this API use JSON. The total page count is read from `page_count`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://www.escrow.com/api/docs/create-customer) |
| [Create Transaction](actions/create-transaction.md) | `POST /transaction` | [docs](https://www.escrow.com/api/docs/create-transaction) |
| [Generate Partner Report](actions/generate-partner-report.md) | `POST /partner/reports` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Check Details](actions/get-check-details.md) | `GET /transaction/:transaction_id/payment_methods/check` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Current Customer](actions/get-current-customer.md) | `GET /customer/me` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:customer_id` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Milestone Item Web URL](actions/get-milestone-item-web-url.md) | `GET /transaction/:transaction_id/item/:item_id/web_link/:action` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get PayPal Landing URL](actions/get-paypal-landing-url.md) | `GET /transaction/:transaction_id/payment_methods/paypal` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Transaction](actions/get-transaction.md) | `GET /transaction/:transaction_id` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Transaction by Reference](actions/get-transaction-by-reference.md) | `GET /transaction/reference/:reference` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Transaction Disbursement Methods](actions/get-transaction-disbursement-methods.md) | `GET /transaction/:transaction_id/disbursement_methods` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Transaction Payment Methods](actions/get-transaction-payment-methods.md) | `GET /transaction/:transaction_id/payment_methods` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Transaction Timeline Entries](actions/get-transaction-timeline-entries.md) | `GET /transaction/:transaction_id/timeline-entries` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Transaction Web URL](actions/get-transaction-web-url.md) | `GET /transaction/:transaction_id/web_link/:action` | [docs](https://www.escrow.com/api/docs/reference) |
| [Get Wire Transfer Details](actions/get-wire-transfer-details.md) | `GET /transaction/:transaction_id/payment_methods/wire_transfer` | [docs](https://www.escrow.com/api/docs/reference) |
| [List Partner Customers](actions/list-partner-customers.md) | `GET /partner/customers` | [docs](https://www.escrow.com/api/docs/reference) |
| [List Partner Transactions](actions/list-partner-transactions.md) | `GET /partner/transactions` | [docs](https://www.escrow.com/api/docs/reference) |
| [List Transactions](actions/list-transactions.md) | `GET /transaction` | [docs](https://www.escrow.com/api/docs/reference) |
| [Patch Transaction Disbursement Method](actions/patch-transaction-disbursement-method.md) | `PATCH /transaction/:transaction_id/disbursement_methods` | [docs](https://www.escrow.com/api/docs/reference) |
| [Perform Milestone Item Action](actions/perform-milestone-item-action.md) | `PATCH /transaction/:transaction_id/item/:item_id` | [docs](https://www.escrow.com/api/docs/reference) |
| [Perform Transaction Action](actions/perform-transaction-action.md) | `PATCH /transaction/:transaction_id` | [docs](https://www.escrow.com/api/docs/reference) |
| [Post Buyer Payment Details](actions/post-buyer-payment-details.md) | `POST /transaction/:transaction_id/buyer_payment` | [docs](https://www.escrow.com/api/docs/reference) |
| [Select Payment Method](actions/select-payment-method.md) | `POST /transaction/:transaction_id/payment_methods/:payment_method_name` | [docs](https://www.escrow.com/api/docs/reference) |
| [Update Current Customer](actions/update-current-customer.md) | `PATCH /customer/me` | [docs](https://www.escrow.com/api/docs/update-customer) |
