# Payfunnels: Native API Reference

A consolidated summary of Payfunnels's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.payfunnels.com/api/docs/
- **API base URL:** `https://api.payfunnels.com`

## Authentication

### API Key

Use a Payfunnels API key sent in the x-pf-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-pf-api-key: <apiKey>
```

[Official authentication documentation](https://api.payfunnels.com/api/docs/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /v1/subscriptions/cancel` | [docs](https://api.payfunnels.com/api/docs/#cancel-subscription) |
| [Create Custom Plan Payment Link](actions/create-custom-plan-payment-link.md) | `POST /v1/paymentlinks/customplan` | [docs](https://api.payfunnels.com/api/docs/#create-custom-plan-payment-link) |
| [Create One-Time Payment Link](actions/create-one-time-payment-link.md) | `POST /v1/paymentlinks/onetime` | [docs](https://api.payfunnels.com/api/docs/#create-one-time-payment-link) |
| [Create Pay What You Want Payment Link](actions/create-pay-what-you-want-payment-link.md) | `POST /v1/paymentlinks/paywhatyouwant` | [docs](https://api.payfunnels.com/api/docs/#create-pay-what-you-want-payment-link) |
| [Create Payment Plan Payment Link](actions/create-payment-plan-payment-link.md) | `POST /v1/paymentlinks/paymentplan` | [docs](https://api.payfunnels.com/api/docs/#create-payment-plan-payment-link) |
| [Create Recurring Payment Link](actions/create-recurring-payment-link.md) | `POST /v1/paymentlinks/recurring` | [docs](https://api.payfunnels.com/api/docs/#create-recurring-payment-link) |
| [Create Setup Fee](actions/create-setup-fee.md) | `POST /v1/fees/setup` | [docs](https://api.payfunnels.com/api/docs/#create-one-time-setup-fees) |
| [Delete Setup Fee](actions/delete-setup-fee.md) | `DELETE /v1/fees/setup/{id}` | [docs](https://api.payfunnels.com/api/docs/#delete-one-time-setup-fees) |
| [Get Payment](actions/get-payment.md) | `GET /v1/payments/{id}` | [docs](https://api.payfunnels.com/api/docs/#returns-payment-by-id) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /v1/paymentlinks/{id}` | [docs](https://api.payfunnels.com/api/docs/#returns-payment-link-by-id) |
| [Get Setup Fee](actions/get-setup-fee.md) | `GET /v1/fees/setup/{id}` | [docs](https://api.payfunnels.com/api/docs/#get-one-time-setup-fees-by-id) |
| [Get Subscription](actions/get-subscription.md) | `GET /v1/subscriptions/{id}` | [docs](https://api.payfunnels.com/api/docs/#returns-subscription-by-id) |
| [List Payment Links](actions/list-payment-links.md) | `GET /v1/paymentlinks` | [docs](https://api.payfunnels.com/api/docs/#returns-list-of-payment-links) |
| [List Payments](actions/list-payments.md) | `GET /v1/payments` | [docs](https://api.payfunnels.com/api/docs/#returns-list-of-payments) |
| [List Setup Fees](actions/list-setup-fees.md) | `GET /v1/fees/setup` | [docs](https://api.payfunnels.com/api/docs/#list-one-time-setup-fees) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/subscriptions` | [docs](https://api.payfunnels.com/api/docs/#returns-list-of-subscriptions) |
| [Pause Subscription](actions/pause-subscription.md) | `POST /v1/subscriptions/pause` | [docs](https://api.payfunnels.com/api/docs/#pause-subscription) |
| [Refund Payment](actions/refund-payment.md) | `POST /v1/payments/refund` | [docs](https://api.payfunnels.com/api/docs/#refund-payment) |
| [Resume Subscription](actions/resume-subscription.md) | `POST /v1/subscriptions/resume` | [docs](https://api.payfunnels.com/api/docs/#resume-subscription) |
| [Update Setup Fee](actions/update-setup-fee.md) | `PUT /v1/fees/setup/{id}` | [docs](https://api.payfunnels.com/api/docs/#update-one-time-setup-fees) |
