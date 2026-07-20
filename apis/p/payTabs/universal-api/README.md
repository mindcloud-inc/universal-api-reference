# <img src="https://images.mindcloud.co/apps/icons/paytabs-icon_1776695922987.png" alt="PayTabs logo" width="28" height="28"> PayTabs: Universal API

PayTabs PT2 payment gateway app for creating payment requests, managing transactions, tokenizing cards, and managing invoices in the global test environment.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/payTabs/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 58
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://paytabs.com
- **Vendor API docs:** https://docs.paytabs.com/manuals/PT-API-Endpoints/Introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Transaction by Reference](actions/query-transaction-by-reference.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-transaction-by-reference?connectionId=$CONNECTION_ID&tran_ref=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (58)

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Invoice](actions/cancel-invoice.md) | PUT |  |
| [Cancel Invoice by Path](actions/cancel-invoice-by-path.md) | PUT |  |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Create Invoice with Payment Methods](actions/create-invoice-with-payment-methods.md) | POST |  |
| [Create Tokenized Invoice](actions/create-tokenized-invoice.md) | POST |  |
| [Download Invoice PDF](actions/download-invoice-pdf.md) | GET |  |
| [Get Invoice Status](actions/get-invoice-status.md) | GET |  |
| [Get Invoice Status by Path](actions/get-invoice-status-by-path.md) | GET |  |
| [Mark Invoice as Paid](actions/mark-invoice-as-paid.md) | PUT |  |
| [Search Invoices](actions/search-invoices.md) | GET |  |
| [Send Invoice SMS](actions/send-invoice-sms.md) | PUT |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create ADCB TouchPoints Payment Page](actions/create-adcb-touchpoints-payment-page.md) | POST |  |
| [Create Alternate Currency Payment Page](actions/create-alternate-currency-payment-page.md) | POST |  |
| [Create Aman Payment Page](actions/create-aman-payment-page.md) | POST |  |
| [Create Donation Payment Page](actions/create-donation-payment-page.md) | POST |  |
| [Create Framed Hosted Payment Page](actions/create-framed-hosted-payment-page.md) | POST |  |
| [Create Halan Payment Page](actions/create-halan-payment-page.md) | POST |  |
| [Create Hosted Payment Page](actions/create-hosted-payment-page.md) | POST |  |
| [Create Hosted Payment Page with Card Approval](actions/create-hosted-payment-page-with-card-approval.md) | POST |  |
| [Create Hosted Payment Page with Card Discounts Amount](actions/create-hosted-payment-page-with-card-discounts-amount.md) | POST |  |
| [Create Hosted Payment Page with Card Discounts Percent and Flat Amount](actions/create-hosted-payment-page-with-card-discounts-percent-and-flat-amount.md) | POST |  |
| [Create Hosted Payment Page with Card Filter](actions/create-hosted-payment-page-with-card-filter.md) | POST |  |
| [Create Hosted Payment Page with Custom Parameters](actions/create-hosted-payment-page-with-custom-parameters.md) | POST |  |
| [Create Hosted Payment Page with Hidden Shipping](actions/create-hosted-payment-page-with-hidden-shipping.md) | POST |  |
| [Create Hosted Payment Page with iFrame PostMessage](actions/create-hosted-payment-page-with-iframe-post-message.md) | POST |  |
| [Create Hosted Payment Page with Invoice](actions/create-hosted-payment-page-with-invoice.md) | POST |  |
| [Create Hosted Payment Page with Theme](actions/create-hosted-payment-page-with-theme.md) | POST |  |
| [Create Hosted Payment Page with Token Info](actions/create-hosted-payment-page-with-token-info.md) | POST |  |
| [Create KNET Payment Page](actions/create-knet-payment-page.md) | POST |  |
| [Create Managed Form Payment](actions/create-managed-form-payment.md) | POST |  |
| [Create MOTO Non-3DS Non-CVV Payment](actions/create-moto-non3ds-non-cvv-payment.md) | POST |  |
| [Create MOTO Non-3DS Payment](actions/create-moto-non3ds-payment.md) | POST |  |
| [Create Optional Tokenizing Hosted Payment Page](actions/create-optional-tokenizing-hosted-payment-page.md) | POST |  |
| [Create Own Form Payment](actions/create-own-form-payment.md) | POST |  |
| [Create PayPal Payment Page](actions/create-paypal-payment-page.md) | POST |  |
| [Create Recurring Payment](actions/create-recurring-payment.md) | POST |  |
| [Create Sadad Split Payout Payment Request](actions/create-sadad-split-payout-payment-request.md) | POST |  |
| [Create Tabby Payment Page](actions/create-tabby-payment-page.md) | POST |  |
| [Create Tamara Payment Page](actions/create-tamara-payment-page.md) | POST |  |
| [Create Token-Based Payment](actions/create-token-based-payment.md) | POST |  |
| [Create Token-Based Payment with Token Info](actions/create-token-based-payment-with-token-info.md) | POST |  |
| [Create Tokenizing Hosted Payment Page](actions/create-tokenizing-hosted-payment-page.md) | POST |  |
| [Query Shopify Transaction by Reference](actions/query-shopify-transaction-by-reference.md) | GET |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Delete Token](actions/delete-token.md) | DELETE |  |
| [Get Token Status](actions/get-token-status.md) | GET |  |
| [Tokenize Card](actions/tokenize-card.md) | POST |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Apple Pay Payment](actions/create-apple-pay-payment.md) | POST |  |
| [Create MOTO Payment](actions/create-moto-payment.md) | POST |  |
| [Create Sadad Payment Request](actions/create-sadad-payment-request.md) | POST |  |
| [Create Samsung Pay Payment](actions/create-samsung-pay-payment.md) | POST |  |
| [Extend Authorization](actions/extend-authorization.md) | PUT |  |
| [Sadad Inquiry](actions/sadad-inquiry.md) | GET |  |
| [ValU Inquiry](actions/valu-inquiry.md) | GET |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Capture Transaction](actions/capture-transaction.md) | PUT |  |
| [Query Transaction by Cart ID](actions/query-transaction-by-cart-id.md) | GET |  |
| [Query Transaction by Reference](actions/query-transaction-by-reference.md) | GET |  |
| [Refund Transaction](actions/refund-transaction.md) | PUT |  |
| [Void Transaction](actions/void-transaction.md) | PUT |  |

