# PayWhirl: Native API Reference

A consolidated summary of PayWhirl's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://api.paywhirl.com/
- **API base URL:** `https://api.paywhirl.com`

## Authentication

### API Key

Authenticate to PayWhirl with your API key and API secret from Settings & Account > Developer > API Keys.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · PayWhirl API secret sent on every request together with the implicit API key credential.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.paywhirl.com/#auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (maximum 100). Use `after_id` in the query string as the pagination cursor.

## Sorting

Set the sort field with `order_key` in the query string. Set the direction separately with `order_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Promo To Invoice](actions/add-promo-to-invoice.md) | `POST /invoice/{id}/add-promo` | [docs](https://api.paywhirl.com/#invoices) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /unsubscribe/customer` | [docs](https://api.paywhirl.com/#subscriptions) |
| [Change Invoice Payment Method](actions/change-invoice-payment-method.md) | `POST /invoice/{id}/card` | [docs](https://api.paywhirl.com/#invoices) |
| [Create Card](actions/create-card.md) | `POST /create/card` | [docs](https://api.paywhirl.com/#charges) |
| [Create Charge](actions/create-charge.md) | `POST /create/charge` | [docs](https://api.paywhirl.com/#charges) |
| [Create Customer](actions/create-customer.md) | `POST /create/customer` | [docs](https://api.paywhirl.com/#customers) |
| [Create Customer Address](actions/create-customer-address.md) | `POST /customer/address` | [docs](https://api.paywhirl.com/#customers) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://api.paywhirl.com/#invoices) |
| [Create Plan](actions/create-plan.md) | `POST /create/plan` | [docs](https://api.paywhirl.com/#plans) |
| [Create Refund](actions/create-refund.md) | `POST /refund/charge/{id}` | [docs](https://api.paywhirl.com/#charges) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscribe/customer` | [docs](https://api.paywhirl.com/#subscriptions) |
| [Delete Card](actions/delete-card.md) | `POST /delete/card` | [docs](https://api.paywhirl.com/#charges) |
| [Delete Customer](actions/delete-customer.md) | `POST /delete/customer` | [docs](https://api.paywhirl.com/#customers) |
| [Delete Customer Address](actions/delete-customer-address.md) | `DELETE /customer/address/{address_id}` | [docs](https://api.paywhirl.com/#customers) |
| [Delete Invoice](actions/delete-invoice.md) | `POST /delete/invoice` | [docs](https://api.paywhirl.com/#invoices) |
| [Get Card](actions/get-card.md) | `GET /card/{id}` | [docs](https://api.paywhirl.com/#charges) |
| [Get Charge](actions/get-charge.md) | `GET /charge/{id}` | [docs](https://api.paywhirl.com/#charges) |
| [Get Customer](actions/get-customer.md) | `GET /customer/{id}` | [docs](https://api.paywhirl.com/#customers) |
| [Get Customer Address](actions/get-customer-address.md) | `GET /customer/address/{id}` | [docs](https://api.paywhirl.com/#customers) |
| [Get Customer Profile](actions/get-customer-profile.md) | `GET /customer/profile/{id}` | [docs](https://api.paywhirl.com/#customers) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoice/{id}` | [docs](https://api.paywhirl.com/#invoices) |
| [Get Plan](actions/get-plan.md) | `GET /plan/{id}` | [docs](https://api.paywhirl.com/#plans) |
| [Get Subscription](actions/get-subscription.md) | `GET /subscription/{id}` | [docs](https://api.paywhirl.com/#subscriptions) |
| [List Customer Addresses](actions/list-customer-addresses.md) | `GET /customer/addresses/{id}` | [docs](https://api.paywhirl.com/#customers) |
| [List Customer Cards](actions/list-customer-cards.md) | `GET /cards/{customer_id}` | [docs](https://api.paywhirl.com/#charges) |
| [List Customer Invoices](actions/list-customer-invoices.md) | `GET /invoices/{customer_id}` | [docs](https://api.paywhirl.com/#invoices) |
| [List Customer Subscriptions](actions/list-customer-subscriptions.md) | `GET /subscriptions/{id}` | [docs](https://api.paywhirl.com/#subscriptions) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://api.paywhirl.com/#customers) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://api.paywhirl.com/#invoices) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://api.paywhirl.com/#plans) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://api.paywhirl.com/#subscriptions) |
| [Mark Invoice As Paid](actions/mark-invoice-as-paid.md) | `POST /invoice/{id}/mark-as-paid` | [docs](https://api.paywhirl.com/#invoices) |
| [Process Invoice](actions/process-invoice.md) | `POST /invoice/{id}/process` | [docs](https://api.paywhirl.com/#invoices) |
| [Remove Promo From Invoice](actions/remove-promo-from-invoice.md) | `POST /invoice/{id}/remove-promo` | [docs](https://api.paywhirl.com/#invoices) |
| [Test Connection](actions/test-connection.md) | `GET /test` | [docs](https://api.paywhirl.com/#auth) |
| [Update Customer](actions/update-customer.md) | `POST /update/customer` | [docs](https://api.paywhirl.com/#customers) |
| [Update Customer Address](actions/update-customer-address.md) | `PATCH /customer/address/{address_id}` | [docs](https://api.paywhirl.com/#customers) |
| [Update Invoice Items](actions/update-invoice-items.md) | `POST /invoice/{id}/items` | [docs](https://api.paywhirl.com/#invoices) |
| [Update Invoice Next Payment Date](actions/update-invoice-next-payment-date.md) | `POST /invoices/{id}/next-payment-date` | [docs](https://api.paywhirl.com/#invoices) |
| [Update Plan](actions/update-plan.md) | `POST /update/plan` | [docs](https://api.paywhirl.com/#plans) |
| [Update Subscription](actions/update-subscription.md) | `POST /update/subscription` | [docs](https://api.paywhirl.com/#subscriptions) |
