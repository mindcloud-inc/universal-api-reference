# Mercado Pago: Native API Reference

A consolidated summary of Mercado Pago's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.mercadopago.com.ar/developers/en/reference
- **API base URL:** `https://api.mercadopago.com`

## Authentication

### Access Token

Mercado Pago Access Token

### Credentials

- **API Key:** `apiKey` · required
- **Public Key:** `publicKey` · optional · Used by Mercado Pago frontend and payment-method flows.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.mercadopago.com/developers/)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Cancellation](actions/create-cancellation.md) | `PUT /v1/payments/{payment_id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_payments_payment_id/put) |
| [Create Preference](actions/create-preference.md) | `POST /checkout/preferences` | [docs](https://www.mercadopago.com.ar/developers/en/reference/preferences/_checkout_preferences/post) |
| [Create Refund](actions/create-refund.md) | `POST /v1/payments/{id}/refunds` | [docs](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_payments_id_refunds/post) |
| [Get Chargeback](actions/get-chargeback.md) | `GET /v1/chargebacks/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_chargebacks_id/get) |
| [Get Claim Details](actions/get-claim-details.md) | `GET /post-purchase/v1/claims/{claim_id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/claims/_claims_id/get) |
| [Get Claim Evidence](actions/get-claim-evidence.md) | `GET /post-purchase/v1/claims/{claim_id}/evidences` | [docs](https://www.mercadopago.com.ar/developers/en/reference/claims/get-claim-evidence/get) |
| [Get Claim History](actions/get-claim-history.md) | `GET /post-purchase/v1/claims/{claim_id}/status_history` | [docs](https://www.mercadopago.com.ar/developers/en/reference/claims/get-claim-history/get) |
| [Get Invoice Data](actions/get-invoice-data.md) | `GET /authorized_payments/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/subscriptions/_authorized_payments_id/get) |
| [Get Merchant Order](actions/get-merchant-order.md) | `GET /merchant_orders/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/merchant_orders/_merchant_orders_id/get) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/{order_id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/orders/_orders_id/get) |
| [Get Payment](actions/get-payment.md) | `GET /v1/payments/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/payments/_payments_id/get) |
| [Get Preference](actions/get-preference.md) | `GET /checkout/preferences/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/preferences/_checkout_preferences_id/get) |
| [Get Refund](actions/get-refund.md) | `GET /v1/payments/{id}/refunds/{refund_id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_payments_id_refunds_refund_id/get) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /v1/payment_methods` | [docs](https://www.mercadopago.com.ar/developers/en/reference/payment_methods/overview) |
| [List Refunds](actions/list-refunds.md) | `GET /v1/payments/{id}/refunds` | [docs](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_payments_id_refunds/get) |
| [Search Claims](actions/search-claims.md) | `GET /post-purchase/v1/claims/search` | [docs](https://www.mercadopago.com.ar/developers/en/reference/claims/search-claims/get) |
| [Search Merchant Orders](actions/search-merchant-orders.md) | `GET /merchant_orders/search` | [docs](https://www.mercadopago.com.ar/developers/en/reference/merchant_orders/_merchant_orders_search/get) |
| [Search Payments](actions/search-payments.md) | `GET /v1/payments/search` | [docs](https://www.mercadopago.com.ar/developers/en/reference/payments/_payments_search/get) |
| [Search Preferences](actions/search-preferences.md) | `GET /checkout/preferences/search` | [docs](https://www.mercadopago.com.ar/developers/en/reference/preferences/_checkout_preferences_search/get) |
| [Search Subscription Plans](actions/search-subscription-plans.md) | `GET /preapproval_plan/search` | [docs](https://www.mercadopago.com.ar/developers/en/reference/subscriptions/_preapproval_plan_search/get) |
| [Search Subscriptions](actions/search-subscriptions.md) | `GET /preapproval/search` | [docs](https://www.mercadopago.com.ar/developers/en/reference/subscriptions/_preapproval_search/get) |
| [Update Merchant Order](actions/update-merchant-order.md) | `PUT /merchant_orders/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/merchant_orders/_merchant_orders_id/put) |
| [Update Preference](actions/update-preference.md) | `PUT /checkout/preferences/{id}` | [docs](https://www.mercadopago.com.ar/developers/en/reference/preferences/_checkout_preferences_id/put) |
