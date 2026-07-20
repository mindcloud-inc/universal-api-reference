# ChargeOver: Native API Reference

A consolidated summary of ChargeOver's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.chargeover.com/docs/api/chargeover-rest-api/
- **OpenAPI specification:** https://developer-docs.chargeover.com/apidocs/openapi/
- **API base URL:** `https://{siteName}.chargeover.com/api/v3`

## Authentication

### API Credential Pair

Use the ChargeOver API credential pair over HTTP Basic Auth. Enter your Public Key in the Username field, your Private Key in the Password field, and your Site Name for the tenant subdomain.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Site Name:** `siteName` · required · Your ChargeOver tenant site name, such as appsmindcloud. This becomes the subdomain in https://{site}.chargeover.com.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.chargeover.com/docs/api-information/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–500). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `equals`, `greaterThan`, `greaterThanOrEqual`, `isNotNull`, `isNull`, `lessThan`, `lessThanOrEqual`, `notEquals`.

## Sorting

Set the sort field with `order` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /package/:package_id/_action/cancel` | [docs](https://developer.chargeover.com/docs/api/cancel-a-subscription/) |
| [Email Invoice](actions/email-invoice.md) | `POST /invoice/:invoice_id/_action/email` | [docs](https://developer.chargeover.com/docs/api/email-an-invoice/) |
| [Email Receipt](actions/email-receipt.md) | `POST /transaction/:transaction_id/_action/email` | [docs](https://developer.chargeover.com/docs/api/email-a-receipt/) |
| [Get Contact](actions/get-contact.md) | `GET /user/:user_id` | [docs](https://developer.chargeover.com/docs/api/get-a-specific-contact/) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:customer_id` | [docs](https://developer.chargeover.com/docs/api/get-a-specific-customer/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoice/:invoice_id` | [docs](https://developer.chargeover.com/docs/api/get-a-specific-invoice/) |
| [Get Invoice PDF](actions/get-invoice-pdf.md) | `POST /invoice/:invoice_id/_action/pdf` | [docs](https://developer.chargeover.com/docs/api/get-a-pdf-of-an-invoice/) |
| [Get Item](actions/get-item.md) | `GET /item/:item_id` | [docs](https://developer.chargeover.com/docs/api/get-a-specific-item/) |
| [Get Subscription](actions/get-subscription.md) | `GET /package/:package_id` | [docs](https://developer.chargeover.com/docs/api/get-a-specific-subscription/) |
| [Get Transaction](actions/get-transaction.md) | `GET /transaction/:transaction_id` | [docs](https://developer.chargeover.com/docs/api/get-a-specific-transaction/) |
| [Invoice Subscription Now](actions/invoice-subscription-now.md) | `POST /package/:package_id/_action/invoice` | [docs](https://developer.chargeover.com/docs/api/invoice-a-subscription-now/) |
| [List Contacts](actions/list-contacts.md) | `GET /user` | [docs](https://developer.chargeover.com/docs/api/query-for-contacts/) |
| [List Customers](actions/list-customers.md) | `GET /customer` | [docs](https://developer.chargeover.com/docs/api/query-for-customers/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoice` | [docs](https://developer.chargeover.com/docs/api/query-for-invoices/) |
| [List Items](actions/list-items.md) | `GET /item` | [docs](https://developer.chargeover.com/docs/api/querying-for-items/) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /package` | [docs](https://developer.chargeover.com/docs/api/querying-for-subscriptions/) |
| [List Transactions](actions/list-transactions.md) | `GET /transaction` | [docs](https://developer.chargeover.com/docs/api/query-for-transactions/) |
| [List Usage Records](actions/list-usage-records.md) | `GET /usage` | [docs](https://developer.chargeover.com/docs/api/query-for-usage-metered-data/) |
| [Record Usage](actions/record-usage.md) | `POST /usage` | [docs](https://developer.chargeover.com/docs/api/storing-usage-metered-data/) |
| [Suspend Subscription](actions/suspend-subscription.md) | `POST /package/:package_id/_action/suspend` | [docs](https://developer.chargeover.com/docs/api/suspend-a-subscription/) |
| [Uncancel Subscription](actions/uncancel-subscription.md) | `POST /package/:package_id/_action/uncancel` | [docs](https://developer.chargeover.com/docs/api/un-cancel-a-subscription/) |
| [Unsuspend Subscription](actions/unsuspend-subscription.md) | `POST /package/:package_id/_action/unsuspend` | [docs](https://developer.chargeover.com/docs/api/unsuspend-a-subscription/) |
| [Void Invoice](actions/void-invoice.md) | `POST /invoice/:invoice_id/_action/void` | [docs](https://developer.chargeover.com/docs/api/void-an-invoice/) |
| [Void Transaction](actions/void-transaction.md) | `POST /transaction/:transaction_id/_action/void` | [docs](https://developer.chargeover.com/docs/api/void-a-transaction/) |
