# Fiserv: Native API Reference

A consolidated summary of Fiserv's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://isvportal.fiserv.com/docs/payments-api
- **OpenAPI specification:** https://docs.getfwd.com/docs/redocusaurus/plugin-redoc-0.yaml
- **API base URL:** `https://bankinghub-cert.fiservapis.com`

## Authentication

### API Key

Authenticate Fiserv Payments API requests with an API key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://isvportal.fiserv.com/docs/payments-api)

### API Key and Secret

Authenticate Banking Hub token requests using HTTP Basic auth with the API key as username and API secret as password.

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

[Official authentication documentation](https://developer.fiserv.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–50). Use `starting_after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Surcharge](actions/calculate-surcharge.md) | `POST /surcharge` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/calculate_surcharge) |
| [Cancel Payment Intent](actions/cancel-payment-intent.md) | `POST /payment_intents/{id}/cancel` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/cancel_payment_intent) |
| [Cancel Payment Method Intent](actions/cancel-payment-method-intent.md) | `POST /payment_method_intents/{id}/cancel` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/cancel_payment_method_intent) |
| [Capture Payment Intent](actions/capture-payment-intent.md) | `POST /payment_intents/{id}/capture` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/capture_payment_intent) |
| [Create Checkout Session](actions/create-checkout-session.md) | `POST /checkout_sessions` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/create_checkout_session) |
| [Create Fee](actions/create-fee.md) | `POST /fees` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/createFee) |
| [Create Payment](actions/create-payment.md) | `POST /payment_intents/{id}/payments` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/create_payment) |
| [Create Payment Intent](actions/create-payment-intent.md) | `POST /payment_intents` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/create_payment_intent) |
| [Create Payment Method Intent](actions/create-payment-method-intent.md) | `POST /payment_method_intents` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/create_payment_method_intent) |
| [Create Refund](actions/create-refund.md) | `POST /payment_intents/{id}/refunds` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/create_refund) |
| [Download Transactions](actions/download-transactions.md) | `POST /transactions/download` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/download_transactions) |
| [Expire Checkout Session](actions/expire-checkout-session.md) | `POST /checkout_sessions/{id}/expire` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/expire_checkout_session) |
| [Fetch Ledger Account Balances](actions/fetch-ledger-account-balances.md) | `GET /balances` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_ledger_account_balances) |
| [Get Banking Hub Access Token](actions/get-banking-hub-access-token.md) | `POST https://bankinghub-cert.fiservapis.com/fts-apim/oauth2/v2` | [docs](https://developer.fiserv.com/) |
| [Get Checkout Session](actions/get-checkout-session.md) | `GET /checkout_sessions/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_checkout_session) |
| [Get Dispute](actions/get-dispute.md) | `GET /disputes/:id` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_dispute) |
| [Get Fee](actions/get-fee.md) | `GET /fees/:id` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/getOneFeeById) |
| [Get Payment](actions/get-payment.md) | `GET /payments/:id` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment) |
| [Get Payment Intent](actions/get-payment-intent.md) | `GET /payment_intents/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_intent) |
| [Get Payment Method](actions/get-payment-method.md) | `GET /payment_methods/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_method) |
| [Get Payment Method Intent](actions/get-payment-method-intent.md) | `GET /payment_method_intents/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_method_intent) |
| [Get Payout](actions/get-payout.md) | `GET /payouts/:id` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payout) |
| [Get Refund](actions/get-refund.md) | `GET /refunds/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_refund) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:id` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_transaction) |
| [List Business Payouts](actions/list-business-payouts.md) | `GET /businesses/payouts` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payouts_by_business) |
| [List Checkout Sessions](actions/list-checkout-sessions.md) | `GET /checkout_sessions` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_checkout_session_list) |
| [List Disputes](actions/list-disputes.md) | `GET /disputes` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_disputes) |
| [List Fees](actions/list-fees.md) | `GET /fees` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/getManyFees) |
| [List Payment Intents](actions/list-payment-intents.md) | `GET /payment_intents` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_intents) |
| [List Payment Method Intents](actions/list-payment-method-intents.md) | `GET /payment_method_intents` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_method_intents) |
| [List Payments For Payment Intent](actions/list-payments-for-payment-intent.md) | `GET /payment_intents/{id}/payments` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/list_payments) |
| [List Payouts](actions/list-payouts.md) | `GET /payouts` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_payouts) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/get_transactions) |
| [List Unmatched Settlements](actions/list-unmatched-settlements.md) | `GET /unmatched_settlements` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/getPartnerUnmatched) |
| [Refund Adhoc Fee](actions/refund-adhoc-fee.md) | `POST /fees/:id/refund` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/createRefund) |
| [Search Payment Intents](actions/search-payment-intents.md) | `POST /payment_intents/search` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/search_payment_intent) |
| [Search Transactions](actions/search-transactions.md) | `POST /transactions/search` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/search_transactions) |
| [Update Checkout Session](actions/update-checkout-session.md) | `PATCH /checkout_sessions/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/update_checkout_session) |
| [Update Payment Intent](actions/update-payment-intent.md) | `PATCH /payment_intents/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/update_payment_intent) |
| [Update Payment Method](actions/update-payment-method.md) | `PATCH /payment_methods/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/update_payment_method) |
| [Update Payment Method Intent](actions/update-payment-method-intent.md) | `PATCH /payment_method_intents/{id}` | [docs](https://isvportal.fiserv.com/docs/payments-api#operation/update_payment_method_intent) |
