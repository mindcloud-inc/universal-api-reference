# Billwerkplus: Native API Reference

A consolidated summary of Billwerkplus's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.frisbii.com/
- **API base URL:** `https://api.frisbii.com/v1`

## Authentication

### API Key

Connect with a private Frisbii API key used as the Basic auth username.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.frisbii.com/docs/api-credentials)

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

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Invoice](actions/cancel-invoice.md) | `POST /invoice/:id/cancel` | [docs](https://docs.frisbii.com/reference/cancelinvoice) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /subscription/:handle/cancel` | [docs](https://docs.frisbii.com/reference/cancelsubscription) |
| [Change Next Renewal Date](actions/change-next-renewal-date.md) | `POST /subscription/:handle/change_next_period_start` | [docs](https://docs.frisbii.com/reference/changenextperiodstartjson) |
| [Change Subscription](actions/change-subscription.md) | `PUT /subscription/:handle` | [docs](https://docs.frisbii.com/reference/changesubscription) |
| [Create Add-On](actions/create-addon.md) | `POST /add_on` | [docs](https://docs.frisbii.com/reference/createaddon) |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://docs.frisbii.com/reference/createcustomerjson) |
| [Create Invoice for Customer](actions/create-invoice-for-customer.md) | `POST /customer/:handle/invoice` | [docs](https://docs.frisbii.com/reference/createcustomerinvoice) |
| [Create On-Demand Subscription Invoice](actions/create-on-demand-subscription-invoice.md) | `POST /subscription/:handle/invoice` | [docs](https://docs.frisbii.com/reference/createsubscriptioninvoice) |
| [Create Plan](actions/create-plan.md) | `POST /plan` | [docs](https://docs.frisbii.com/reference/createplanjson) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscription` | [docs](https://docs.frisbii.com/reference/createsubscriptionjson) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customer/:handle` | [docs](https://docs.frisbii.com/reference/deletecustomer) |
| [Get Add-On](actions/get-add-on.md) | `GET /add_on/:handle` | [docs](https://docs.frisbii.com/reference/getaddon) |
| [Get Charge](actions/get-charge.md) | `GET /charge/:handle` | [docs](https://docs.frisbii.com/reference/getcharge) |
| [Get Account](actions/get-current-account.md) | `GET /account` | [docs](https://docs.frisbii.com/reference/getcurrentaccount) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:handle` | [docs](https://docs.frisbii.com/reference/getcustomer) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoice/:id` | [docs](https://docs.frisbii.com/reference/getinvoice) |
| [Get Plan](actions/get-plan.md) | `GET /plan/:handle/current` | [docs](https://docs.frisbii.com/reference/getcurrentplan) |
| [Get Subscription](actions/get-subscription.md) | `GET /subscription/:handle` | [docs](https://docs.frisbii.com/reference/getsubscription) |
| [Get Subscription Payment Method](actions/get-subscription-payment-method.md) | `GET /subscription/:handle/pm` | [docs](https://docs.frisbii.com/reference/getsubscriptionpaymentmethod) |
| [List Add-Ons](actions/list-add-ons.md) | `GET /list/add_on` | [docs](https://docs.frisbii.com/reference/getaddonlist) |
| [List Charges](actions/list-charges.md) | `GET /list/charge` | [docs](https://docs.frisbii.com/reference/getchargelist) |
| [List Customers](actions/list-customers.md) | `GET /list/customer` | [docs](https://docs.frisbii.com/reference/getcustomerlist) |
| [List Disputes](actions/list-disputes.md) | `GET /list/dispute` | [docs](https://docs.frisbii.com/reference/getdisputelist) |
| [List Invoices](actions/list-invoices.md) | `GET /list/invoice` | [docs](https://docs.frisbii.com/reference/getinvoicelist) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /list/payment_method` | [docs](https://docs.frisbii.com/reference/getpaymentmethodlist) |
| [List Plans](actions/list-plans.md) | `GET /list/plan` | [docs](https://docs.frisbii.com/reference/getplanlist) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /list/subscription` | [docs](https://docs.frisbii.com/reference/getsubscriptionlist) |
| [Preview Next Subscription Invoice](actions/preview-next-subscription-invoice.md) | `GET /subscription/:handle/next_invoice_preview` | [docs](https://docs.frisbii.com/reference/previewnextsubscriptioninvoice) |
| [Put Subscription On Hold](actions/put-subscription-on-hold.md) | `POST /subscription/:handle/on_hold` | [docs](https://docs.frisbii.com/reference/onhold) |
| [Reactivate Invoice](actions/reactivate-invoice.md) | `POST /invoice/:id/reactivate` | [docs](https://docs.frisbii.com/reference/reactivateinvoice) |
| [Reactivate Subscription](actions/reactivate-subscription.md) | `POST /subscription/:handle/reactivate` | [docs](https://docs.frisbii.com/reference/reactivatesubscription) |
| [Update Add-On](actions/update-addon.md) | `PUT /add_on/:handle` | [docs](https://docs.frisbii.com/reference/updateaddon) |
| [Update Customer](actions/update-customer.md) | `PUT /customer/:handle` | [docs](https://docs.frisbii.com/reference/updatecustomerjson) |
