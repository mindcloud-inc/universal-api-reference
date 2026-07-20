# ChargeBee: Native API Reference

A consolidated summary of ChargeBee's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.chargebee.com/docs/api
- **API base URL:** `https://{baseUrl}.chargebee.com/api/v2/`

## Authentication

### Chargebee API Key

Connect with a Chargebee test or live site name and an API key. Chargebee uses HTTP Basic authentication with the API key as the username and an empty password.

### Credentials

- **API Key:** `apiKey` · required · Chargebee API key. Chargebee uses this as the HTTP Basic username with an empty password.
- **Site Name:** `baseUrl` · required · Chargebee site subdomain only, for example acme-test from https://acme-test.chargebee.com.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://apidocs.chargebee.com/docs/api/auth)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. The next-page cursor is read from `next_offset`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST customers` | [docs](https://apidocs.chargebee.com/docs/api/customers/create-a-customer) |
| [List Business Entities](actions/list-business-entities.md) | `GET business_entities` | [docs](https://apidocs.chargebee.com/docs/api/business-entities/list-business-entities) |
| [List Coupons](actions/list-coupons.md) | `GET coupons` | [docs](https://apidocs.chargebee.com/docs/api/coupons/list-coupons) |
| [List Credit Notes](actions/list-credit-notes.md) | `GET credit_notes` | [docs](https://apidocs.chargebee.com/docs/api/credit-notes/list-credit-notes) |
| [List Customers](actions/list-customers.md) | `GET customers` | [docs](https://apidocs.chargebee.com/docs/api/customers/list-customers) |
| [List Events](actions/list-events.md) | `GET events` | [docs](https://apidocs.chargebee.com/docs/api/events/list-events) |
| [List Hosted Pages](actions/list-hosted-pages.md) | `GET hosted_pages` | [docs](https://apidocs.chargebee.com/docs/api/hosted-pages/list-hosted-pages) |
| [List Invoices](actions/list-invoices.md) | `GET invoices` | [docs](https://apidocs.chargebee.com/docs/api/invoices/list-invoices) |
| [List Item Prices](actions/list-item-prices.md) | `GET item_prices` | [docs](https://apidocs.chargebee.com/docs/api/item-prices/list-item-prices) |
| [List Items](actions/list-items.md) | `GET items` | [docs](https://apidocs.chargebee.com/docs/api/items/list-items) |
| [List Orders](actions/list-orders.md) | `GET orders` | [docs](https://apidocs.chargebee.com/docs/api/orders/list-orders) |
| [List Payment Sources](actions/list-payment-sources.md) | `GET payment_sources` | [docs](https://apidocs.chargebee.com/docs/api/payment-sources/list-payment-sources) |
| [List Promotional Credits](actions/list-promotional-credits.md) | `GET promotional_credits` | [docs](https://apidocs.chargebee.com/docs/api/promotional-credits/list-promotional-credits) |
| [List Quotes](actions/list-quotes.md) | `GET quotes` | [docs](https://apidocs.chargebee.com/docs/api/quotes/list-quotes) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET subscriptions` | [docs](https://apidocs.chargebee.com/docs/api/subscriptions/list-subscriptions) |
| [List Transactions](actions/list-transactions.md) | `GET transactions` | [docs](https://apidocs.chargebee.com/docs/api/transactions/list-transactions) |
| [List Unbilled Charges](actions/list-unbilled-charges.md) | `GET unbilled_charges` | [docs](https://apidocs.chargebee.com/docs/api/unbilled-charges/list-unbilled-charges) |
| [List Usages](actions/list-usages.md) | `GET usages` | [docs](https://apidocs.chargebee.com/docs/api/usages/list-usages) |
| [List Virtual Bank Accounts](actions/list-virtual-bank-accounts.md) | `GET virtual_bank_accounts` | [docs](https://apidocs.chargebee.com/docs/api/virtual-bank-accounts/list-virtual-bank-accounts) |
| [Retrieve Business Entity](actions/retrieve-business-entity.md) | `GET business_entities/:business_entity_id` | [docs](https://apidocs.chargebee.com/docs/api/business-entities/retrieve-a-business-entity) |
| [Retrieve Coupon](actions/retrieve-coupon.md) | `GET coupons/:coupon_id` | [docs](https://apidocs.chargebee.com/docs/api/coupons/retrieve-a-coupon) |
| [Retrieve Credit Note](actions/retrieve-credit-note.md) | `GET credit_notes/:credit_note_id` | [docs](https://apidocs.chargebee.com/docs/api/credit-notes/retrieve-a-credit-note) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET customers/:customer_id` | [docs](https://apidocs.chargebee.com/docs/api/customers/retrieve-a-customer) |
| [Retrieve Event](actions/retrieve-event.md) | `GET events/:event_id` | [docs](https://apidocs.chargebee.com/docs/api/events/retrieve-an-event) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET invoices/:invoice_id` | [docs](https://apidocs.chargebee.com/docs/api/invoices/retrieve-an-invoice) |
| [Retrieve Item](actions/retrieve-item.md) | `GET items/:item_id` | [docs](https://apidocs.chargebee.com/docs/api/items/retrieve-an-item) |
| [Retrieve Item Price](actions/retrieve-item-price.md) | `GET item_prices/:item_price_id` | [docs](https://apidocs.chargebee.com/docs/api/item-prices/retrieve-an-item-price) |
| [Retrieve Payment Source](actions/retrieve-payment-source.md) | `GET payment_sources/:payment_source_id` | [docs](https://apidocs.chargebee.com/docs/api/payment-sources/retrieve-a-payment-source) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET subscriptions/:subscription_id` | [docs](https://apidocs.chargebee.com/docs/api/subscriptions/retrieve-a-subscription) |
| [Retrieve Transaction](actions/retrieve-transaction.md) | `GET transactions/:transaction_id` | [docs](https://apidocs.chargebee.com/docs/api/transactions/retrieve-a-transaction) |
| [Update Customer](actions/update-customer.md) | `POST customers/:customer_id` | [docs](https://apidocs.chargebee.com/docs/api/customers/update-a-customer) |
