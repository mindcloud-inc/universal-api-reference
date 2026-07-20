# Reepay: Native API Reference

A consolidated summary of Reepay's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.frisbii.com/reference
- **OpenAPI specification:** https://api.reepay.com/openapi.json
- **API base URL:** `https://api.frisbii.com`

## Authentication

### Private API Key

Authenticate Reepay with HTTP Basic auth using the private API key as the username and an empty password.

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

[Official authentication documentation](https://docs.frisbii.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 10–100). Use `next_page_token` in the query string as the pagination cursor.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Offline Payment Method](actions/add-offline-payment-method.md) | `POST /v1/payment_method/offline` | [docs](https://docs.frisbii.com/reference/addofflinepaymentmethod) |
| [Add Payment Method](actions/add-payment-method.md) | `POST /v1/payment_method` | [docs](https://docs.frisbii.com/reference/addpaymentmethodv2) |
| [Cancel Charge](actions/cancel-charge.md) | `POST /v1/charge/:handle/cancel` | [docs](https://docs.frisbii.com/reference/cancelcharge) |
| [Cancel Invoice](actions/cancel-invoice.md) | `POST /v1/invoice/:id/cancel` | [docs](https://docs.frisbii.com/reference/cancelinvoice) |
| [Cancel Invoice Transaction](actions/cancel-invoice-transaction.md) | `POST /v1/invoice/:id/transaction/:transaction/cancel` | [docs](https://docs.frisbii.com/reference/canceltransaction) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /v1/subscription/:handle/cancel` | [docs](https://docs.frisbii.com/reference/cancelsubscription) |
| [Create Charge](actions/create-charge.md) | `POST /v1/charge` | [docs](https://docs.frisbii.com/reference/createcharge) |
| [Create Customer](actions/create-customer.md) | `POST /v1/customer` | [docs](https://docs.frisbii.com/reference/createcustomerjson) |
| [Create Offline Agreement](actions/create-offline-agreement.md) | `POST /v1/agreement/offline` | [docs](https://docs.frisbii.com/reference/createofflineagreement) |
| [Create Plan](actions/create-plan.md) | `POST /v1/plan` | [docs](https://docs.frisbii.com/reference/createplanjson) |
| [Create Subscription](actions/create-subscription.md) | `POST /v1/subscription` | [docs](https://docs.frisbii.com/reference/createsubscriptionjson) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /v1/customer/:handle` | [docs](https://docs.frisbii.com/reference/deletecustomer) |
| [Delete Gateway Agreement](actions/delete-gateway-agreement.md) | `DELETE /v1/agreement/:id` | [docs](https://docs.frisbii.com/reference/deletegatewayagreement) |
| [Delete Payment Method](actions/delete-payment-method.md) | `DELETE /v1/payment_method/:id` | [docs](https://docs.frisbii.com/reference/deletepaymentmethodv2) |
| [Delete Pending Subscription](actions/delete-pending-subscription.md) | `DELETE /v1/subscription/:handle` | [docs](https://docs.frisbii.com/reference/deletepending) |
| [Delete Plan](actions/delete-plan.md) | `DELETE /v1/plan/:handle` | [docs](https://docs.frisbii.com/reference/deleteplan) |
| [Get Charge](actions/get-charge.md) | `GET /v1/charge/:handle` | [docs](https://docs.frisbii.com/reference/getcharge) |
| [Get Current Plan](actions/get-current-plan.md) | `GET /v1/plan/:handle/current` | [docs](https://docs.frisbii.com/reference/getcurrentplan) |
| [Get Customer](actions/get-customer.md) | `GET /v1/customer/:handle` | [docs](https://docs.frisbii.com/reference/getcustomer) |
| [Get Gateway Agreement](actions/get-gateway-agreement.md) | `GET /v1/agreement/:id` | [docs](https://docs.frisbii.com/reference/getgatewayagreement) |
| [Get Invoice](actions/get-invoice.md) | `GET /v1/invoice/:id` | [docs](https://docs.frisbii.com/reference/getinvoice) |
| [Get Payment Method](actions/get-payment-method.md) | `GET /v1/payment_method/:id` | [docs](https://docs.frisbii.com/reference/getpaymentmethodv2) |
| [Get Subscription](actions/get-subscription.md) | `GET /v1/subscription/:handle` | [docs](https://docs.frisbii.com/reference/getsubscription) |
| [List Charges](actions/list-charges.md) | `GET /v1/list/charge` | [docs](https://docs.frisbii.com/reference/getchargelist) |
| [List Customers](actions/list-customers.md) | `GET /v1/list/customer` | [docs](https://docs.frisbii.com/reference/getcustomerlist) |
| [List Invoices](actions/list-invoices.md) | `GET /v1/list/invoice` | [docs](https://docs.frisbii.com/reference/getinvoicelist) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /v1/list/payment_method` | [docs](https://docs.frisbii.com/reference/getpaymentmethodlist) |
| [List Plans](actions/list-plans.md) | `GET /v1/list/plan` | [docs](https://docs.frisbii.com/reference/getplanlist) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/list/subscription` | [docs](https://docs.frisbii.com/reference/getsubscriptionlist) |
| [Update Customer](actions/update-customer.md) | `PUT /v1/customer/:handle` | [docs](https://docs.frisbii.com/reference/updatecustomerjson) |
| [Update Plan](actions/update-plan.md) | `PUT /v1/plan/:handle` | [docs](https://docs.frisbii.com/reference/updateplanjson) |
| [Update Subscription](actions/update-subscription.md) | `PUT /v1/subscription/:handle` | [docs](https://docs.frisbii.com/reference/changesubscription) |
