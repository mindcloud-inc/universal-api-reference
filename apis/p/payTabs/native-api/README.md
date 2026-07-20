# PayTabs: Native API Reference

A consolidated summary of PayTabs's API configuration and 58 documented operations, with links to official documentation.

- **Official docs:** https://docs.paytabs.com/manuals/PT-API-Endpoints/Introduction/
- **API base URL:** `{apiBaseUrl}`

## Authentication

### PayTabs Server Key

Use the PayTabs PT2 server key, client key, matching profile ID, and region-specific secure base URL.

### Credentials

- **API Key:** `apiKey` · required · PT2 server key from Developers > API Keys > Key management.
- **Profile ID:** `profileId` · required · PayTabs profile ID paired with the server key.
- **API Base URL:** `apiBaseUrl` · required · Region-specific secure PayTabs base URL, for example https://secure-global.paytabs.com.
- **Client Key:** `clientKey` · required · PayTabs PT2 client key used by tokenisation and managed-form flows.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://support.paytabs.com/en/support/solutions/articles/60000978872-step-2-hosted-payment-page-apis-configure-the-integration-method)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (58 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Invoice](actions/cancel-invoice.md) | `POST /payment/invoice/cancel` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Cancel-Invoice/) |
| [Cancel Invoice by Path](actions/cancel-invoice-by-path.md) | `PUT /payment/invoice/{invoice_id}/cancel` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Capture Transaction](actions/capture-transaction.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Capture-Transaction/) |
| [Create ADCB TouchPoints Payment Page](actions/create-adcb-touchpoints-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Alternate Currency Payment Page](actions/create-alternate-currency-payment-page.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Aman Payment Page](actions/create-aman-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Apple Pay Payment](actions/create-apple-pay-payment.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Donation Payment Page](actions/create-donation-payment-page.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Framed Hosted Payment Page](actions/create-framed-hosted-payment-page.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Halan Payment Page](actions/create-halan-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Hosted Payment Page](actions/create-hosted-payment-page.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Card Approval](actions/create-hosted-payment-page-with-card-approval.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Card Discounts Amount](actions/create-hosted-payment-page-with-card-discounts-amount.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Card Discounts Percent and Flat Amount](actions/create-hosted-payment-page-with-card-discounts-percent-and-flat-amount.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Card Filter](actions/create-hosted-payment-page-with-card-filter.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Custom Parameters](actions/create-hosted-payment-page-with-custom-parameters.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Hidden Shipping](actions/create-hosted-payment-page-with-hidden-shipping.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with iFrame PostMessage](actions/create-hosted-payment-page-with-iframe-post-message.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Invoice](actions/create-hosted-payment-page-with-invoice.md) | `POST /payment/request` | [docs](https://support.paytabs.com/en/support/solutions/articles/60000929703-3-2-2-invoices-apis-initiating-creating-the-invoice-payment-request-via-payment-endpoint-) |
| [Create Hosted Payment Page with Theme](actions/create-hosted-payment-page-with-theme.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Hosted Payment Page with Token Info](actions/create-hosted-payment-page-with-token-info.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Invoice](actions/create-invoice.md) | `POST /payment/new/invoice` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-3-Initiating-the-payment/Invoices-Step-3-Initiating-the-payment-Landing/) |
| [Create Invoice with Payment Methods](actions/create-invoice-with-payment-methods.md) | `POST /payment/invoice/new` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create KNET Payment Page](actions/create-knet-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Managed Form Payment](actions/create-managed-form-payment.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Managed-Form/Managed-Form-Step-3-Initiating-the-payment/Managed-Form-Step-3-Landing/) |
| [Create MOTO Non-3DS Non-CVV Payment](actions/create-moto-non3ds-non-cvv-payment.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create MOTO Non-3DS Payment](actions/create-moto-non3ds-payment.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create MOTO Payment](actions/create-moto-payment.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Optional Tokenizing Hosted Payment Page](actions/create-optional-tokenizing-hosted-payment-page.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Create Own Form Payment](actions/create-own-form-payment.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Own-Form/Own-Form-Step-3-Initiating-the-payment/Own-Form-Step-3-Landing/) |
| [Create PayPal Payment Page](actions/create-paypal-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Recurring Payment](actions/create-recurring-payment.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Token-Based-Transactions/Step-2-Using-Token/Token-Based-Transactions-Recurring/) |
| [Create Sadad Payment Request](actions/create-sadad-payment-request.md) | `POST /payment/apm/sadad/ifs/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Sadad Split Payout Payment Request](actions/create-sadad-split-payout-payment-request.md) | `POST /payment/apm/sadad/ifs/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Samsung Pay Payment](actions/create-samsung-pay-payment.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Tabby Payment Page](actions/create-tabby-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Tamara Payment Page](actions/create-tamara-payment-page.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Token-Based Payment](actions/create-token-based-payment.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Token-Based-Transactions/Step-2-Using-Token/Token-Based-Transactions-CVV-Only/) |
| [Create Token-Based Payment with Token Info](actions/create-token-based-payment-with-token-info.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Token-Based-Transactions/Step-2-Using-Token/Token-Based-Transactions-CVV-Only/) |
| [Create Tokenized Invoice](actions/create-tokenized-invoice.md) | `POST /payment/new/invoice` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Create Tokenizing Hosted Payment Page](actions/create-tokenizing-hosted-payment-page.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-3-Initiating-the-payment/HPP-Step-3-Landing/) |
| [Delete Token](actions/delete-token.md) | `POST /payment/token/delete` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Token-Based-Transactions/Step-3-Managing-Token/Token-Based-Transactions-Delete-Token/) |
| [Download Invoice PDF](actions/download-invoice-pdf.md) | `GET /payment/invoice/{invoice_id}/download/pdf` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Downloading-Invoice/) |
| [Extend Authorization](actions/extend-authorization.md) | `POST /payment/request` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Get Invoice Status](actions/get-invoice-status.md) | `POST /payment/invoice/status` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Invoice-status/) |
| [Get Invoice Status by Path](actions/get-invoice-status-by-path.md) | `GET /payment/invoice/{invoice_id}/status` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Get Token Status](actions/get-token-status.md) | `POST /payment/token` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Token-Based-Transactions/Step-3-Managing-Token/Token-Based-Transactions-Get-Status/) |
| [Mark Invoice as Paid](actions/mark-invoice-as-paid.md) | `POST /payment/invoice/paid` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Invoice-external-payment/) |
| [Query Shopify Transaction by Reference](actions/query-shopify-transaction-by-reference.md) | `POST /payment/query` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Query-Transaction/) |
| [Query Transaction by Cart ID](actions/query-transaction-by-cart-id.md) | `POST /payment/query` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Query-Transaction/) |
| [Query Transaction by Reference](actions/query-transaction-by-reference.md) | `POST /payment/query` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Query-Transaction/) |
| [Refund Transaction](actions/refund-transaction.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Refund-Transaction/) |
| [Sadad Inquiry](actions/sadad-inquiry.md) | `POST /payment/apm/sadad/ifs/inquiry` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Search Invoices](actions/search-invoices.md) | `POST /payment/invoice/search` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Search-Invoices-List/) |
| [Send Invoice SMS](actions/send-invoice-sms.md) | `POST /payment/invoice/{invoice_id}/sms` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Send-Invoice-by-SMS/) |
| [Tokenize Card](actions/tokenize-card.md) | `POST /payment/tokenise` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Managed-Form/Managed-Form-Step-4-Accepting-the-payment/Managed-Form-Step-4-Landing/) |
| [ValU Inquiry](actions/valu-inquiry.md) | `POST /payment/info/valu/inquiry` | [docs](https://documenter.getpostman.com/view/14575178/TWDRtfWG) |
| [Void Transaction](actions/void-transaction.md) | `POST /payment/request` | [docs](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Void-Transaction/) |
