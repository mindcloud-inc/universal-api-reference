# Copperx: Native API Reference

A consolidated summary of Copperx's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://copperx.readme.io/reference
- **API base URL:** `https://api.copperx.dev/api/v1`

## Authentication

### Copperx API Key

Use a Copperx API key. Copperx requires Authorization: Bearer <api_key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://copperx.readme.io/reference/authcontroller_getcurrentuser)

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Payment Link](actions/activate-payment-link.md) | `POST /payment-links/{linkId}/activate` | [docs](https://copperx.readme.io/reference/paymentlinkcontroller_activate) |
| [Activate Product](actions/activate-product.md) | `POST /products/{id}/activate` | [docs](https://copperx.readme.io/reference/productcontroller_activate) |
| [Deactivate Payment Link](actions/deactivate-payment-link.md) | `POST /payment-links/{linkId}/deactivate` | [docs](https://copperx.readme.io/reference/paymentlinkcontroller_deactivate) |
| [Deactivate Product](actions/deactivate-product.md) | `POST /products/{id}/deactivate` | [docs](https://copperx.readme.io/reference/productcontroller_deactivate) |
| [Duplicate Invoice](actions/duplicate-invoice.md) | `POST /invoices/{id}/duplicate` | [docs](https://copperx.readme.io/reference/invoicecontroller_duplicateinvoice) |
| [Finalize Invoice](actions/finalize-invoice.md) | `POST /invoices/{id}/finalize` | [docs](https://copperx.readme.io/reference/invoicecontroller_finalizeinvoice) |
| [Get Checkout Session](actions/get-checkout-session.md) | `GET /checkout/sessions/{id}` | [docs](https://copperx.readme.io/reference/sessionscontroller_findone) |
| [Get Current User](actions/get-current-user.md) | `GET /auth/me` | [docs](https://copperx.readme.io/reference/authcontroller_getcurrentuser) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{id}` | [docs](https://copperx.readme.io/reference/customercontroller_get) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/{id}` | [docs](https://copperx.readme.io/reference/invoicecontroller_get) |
| [Get Organization Info](actions/get-organization-info.md) | `GET /organization` | [docs](https://copperx.readme.io/reference/organizationcontroller_getorganizationinfo) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /payment-links/{linkId}` | [docs](https://copperx.readme.io/reference/paymentlinkcontroller_get) |
| [Get Payment Setting](actions/get-payment-setting.md) | `GET /organization/payment-setting` | [docs](https://copperx.readme.io/reference/paymentsettingcontroller_get) |
| [Get Price](actions/get-price.md) | `GET /prices/{id}` | [docs](https://copperx.readme.io/reference/pricecontroller_get) |
| [Get Price Constants](actions/get-price-constants.md) | `GET /constants/prices` | [docs](https://copperx.readme.io/reference/constantscontroller_getprices) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://copperx.readme.io/reference/productcontroller_get) |
| [Get Subscription](actions/get-subscription.md) | `GET /subscriptions/{id}` | [docs](https://copperx.readme.io/reference/subscriptioncontroller_get) |
| [Get Tax Rate](actions/get-tax-rate.md) | `GET /tax-rates/{id}` | [docs](https://copperx.readme.io/reference/taxratecontroller_get) |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | `GET /webhook-endpoints/{id}` | [docs](https://copperx.readme.io/reference/webhookendpointcontroller_get) |
| [Get Withdrawal Address](actions/get-withdrawal-address.md) | `GET /organization/withdrawal-addresses/{id}` | [docs](https://copperx.readme.io/reference/withdrawaladdresscontroller_get) |
| [List Assets](actions/list-assets.md) | `GET /assets` | [docs](https://copperx.readme.io/reference/assetcontroller_findall) |
| [List Chains](actions/list-chains.md) | `GET /chains` | [docs](https://copperx.readme.io/reference/chaincontroller_findall) |
| [List Checkout Sessions](actions/list-checkout-sessions.md) | `GET /checkout/sessions` | [docs](https://copperx.readme.io/reference/sessionscontroller_findall) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://copperx.readme.io/reference/customercontroller_findall) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://copperx.readme.io/reference/invoicecontroller_getall) |
| [List Payment Links](actions/list-payment-links.md) | `GET /payment-links` | [docs](https://copperx.readme.io/reference/paymentlinkcontroller_findall) |
| [List Prices](actions/list-prices.md) | `GET /prices` | [docs](https://copperx.readme.io/reference/pricecontroller_findall) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://copperx.readme.io/reference/productcontroller_findall) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://copperx.readme.io/reference/subscriptioncontroller_findall) |
| [List Tax Rates](actions/list-tax-rates.md) | `GET /tax-rates` | [docs](https://copperx.readme.io/reference/taxratecontroller_findall) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://copperx.readme.io/reference/transactioncontroller_findall) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /webhook-endpoints` | [docs](https://copperx.readme.io/reference/webhookendpointcontroller_getall) |
| [List Withdrawal Addresses](actions/list-withdrawal-addresses.md) | `GET /organization/withdrawal-addresses` | [docs](https://copperx.readme.io/reference/withdrawaladdresscontroller_getall) |
| [Send Invoice](actions/send-invoice.md) | `POST /invoices/{id}/send` | [docs](https://copperx.readme.io/reference/invoicecontroller_finalizeandsendinvoice) |
| [Void Invoice](actions/void-invoice.md) | `POST /invoices/{id}/void` | [docs](https://copperx.readme.io/reference/invoicecontroller_voidinvoice) |
