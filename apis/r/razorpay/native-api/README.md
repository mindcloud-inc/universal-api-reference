# Razorpay: Native API Reference

A consolidated summary of Razorpay's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://razorpay.com/docs/api/
- **API base URL:** `https://api.razorpay.com`

## Authentication

### Basic Auth

Authenticate Razorpay API requests using Key ID and Key Secret as basic auth credentials.

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

[Official authentication documentation](https://razorpay.com/docs/api/authentication/)

## API conventions

Response data is read from `items`.

## Pagination

Use `count` in the query string to set the page size (default 10; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Dispute](actions/accept-dispute.md) | `POST /v1/disputes/:id/accept` | [docs](https://razorpay.com/docs/api/disputes/accept/) |
| [Capture Payment](actions/capture-payment.md) | `POST /v1/payments/:id/capture` | [docs](https://razorpay.com/docs/api/payments/capture/) |
| [Create Customer](actions/create-customer.md) | `POST /v1/customers` | [docs](https://razorpay.com/docs/api/customers/create/) |
| [Create Order](actions/create-order.md) | `POST /v1/orders` | [docs](https://razorpay.com/docs/api/orders/create/) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /v1/payment_links` | [docs](https://razorpay.com/docs/api/payments/payment-links/create-standard/) |
| [Create Payment Refund](actions/create-payment-refund.md) | `POST /v1/payments/:id/refund` | [docs](https://razorpay.com/docs/api/refunds/create-normal/) |
| [Get Dispute](actions/get-dispute.md) | `GET /v1/disputes/:id` | [docs](https://razorpay.com/docs/api/disputes/fetch/) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/:id` | [docs](https://razorpay.com/docs/api/orders/fetch-with-id/) |
| [Get Payment](actions/get-payment.md) | `GET /v1/payments/:id` | [docs](https://razorpay.com/docs/api/payments/fetch-with-id/) |
| [Get Payment Card Details](actions/get-payment-card-details.md) | `GET /v1/payments/:id/card` | [docs](https://razorpay.com/docs/api/payments/fetch-card-details-payment/) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /v1/payment_links/:id` | [docs](https://razorpay.com/docs/api/payments/payment-links/fetch-id-standard/) |
| [Get Refund](actions/get-refund.md) | `GET /v1/refunds/:id` | [docs](https://razorpay.com/docs/api/refunds/fetch-with-id/) |
| [Get Settlement](actions/get-settlement.md) | `GET /v1/settlements/:id` | [docs](https://razorpay.com/docs/api/settlements/fetch-with-id/) |
| [List Customers](actions/list-customers.md) | `GET /v1/customers` | [docs](https://razorpay.com/docs/api/customers/fetch-all/) |
| [List Disputes](actions/list-disputes.md) | `GET /v1/disputes` | [docs](https://razorpay.com/docs/api/disputes/fetch-all/) |
| [List Order Payments](actions/list-order-payments.md) | `GET /v1/orders/:id/payments` | [docs](https://razorpay.com/docs/api/orders/fetch-payments/) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://razorpay.com/docs/api/orders/fetch-all/) |
| [List Payment Links](actions/list-payment-links.md) | `GET /v1/payment_links/` | [docs](https://razorpay.com/docs/api/payments/payment-links/fetch-all-standard/) |
| [List Payment Refunds](actions/list-payment-refunds.md) | `GET /v1/payments/:id/refunds` | [docs](https://razorpay.com/docs/api/refunds/fetch-multiple-refund-payment/) |
| [List Payments](actions/list-payments.md) | `GET /v1/payments` | [docs](https://razorpay.com/docs/api/payments/fetch-all-payments/) |
| [List Refunds](actions/list-refunds.md) | `GET /v1/refunds/` | [docs](https://razorpay.com/docs/api/refunds/fetch-all/) |
| [List Settlements](actions/list-settlements.md) | `GET /v1/settlements/` | [docs](https://razorpay.com/docs/api/settlements/fetch-all/) |
| [Update Customer](actions/update-customer.md) | `PUT /v1/customers/:id` | [docs](https://razorpay.com/docs/api/customers/edit/) |
| [Update Payment Link](actions/update-payment-link.md) | `PATCH /v1/payment_links/:id` | [docs](https://razorpay.com/docs/api/payments/payment-links/update-standard/) |
