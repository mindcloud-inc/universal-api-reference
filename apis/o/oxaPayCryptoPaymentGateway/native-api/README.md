# OxaPay Crypto Payment Gateway: Native API Reference

A consolidated summary of OxaPay Crypto Payment Gateway's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.oxapay.com
- **API base URL:** `https://api.oxapay.com/v1`

## Authentication

### Merchant API Key

Use your OxaPay Merchant API key. OxaPay merchant endpoints authenticate with the exact header merchant_api_key.

### Credentials

- **API Key:** `apiKey` · optional · OxaPay Merchant API key.

[Official authentication documentation](https://docs.oxapay.com/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Invoice](actions/generate-invoice.md) | `POST /payment/invoice` | [docs](https://docs.oxapay.com/api-reference/payment/generate-invoice) |
| [Generate Static Address](actions/generate-static-address.md) | `POST /payment/static-address` | [docs](https://docs.oxapay.com/api-reference/payment/generate-static-address) |
| [Generate White Label](actions/generate-white-label.md) | `POST /payment/white-label` | [docs](https://docs.oxapay.com/api-reference/payment/generate-white-label2) |
| [Get Payment](actions/get-payment.md) | `GET /payment/:track_id` | [docs](https://docs.oxapay.com/api-reference/payment/payment-information) |
| [Get System Status](actions/get-system-status.md) | `GET /common/monitor` | [docs](https://docs.oxapay.com/api-reference/common/system-status) |
| [List Accepted Currencies](actions/list-accepted-currencies.md) | `GET /payment/accepted-currencies` | [docs](https://docs.oxapay.com/api-reference/payment/accepted-currencies) |
| [List Payments](actions/list-payments.md) | `GET /payment` | [docs](https://docs.oxapay.com/api-reference/payment/payment-history) |
| [List Prices](actions/list-prices.md) | `GET /common/prices` | [docs](https://docs.oxapay.com/api-reference/common/prices2) |
| [List Static Addresses](actions/list-static-addresses.md) | `GET /payment/static-address` | [docs](https://docs.oxapay.com/api-reference/payment/static-address-list) |
| [List Supported Currencies](actions/list-supported-currencies.md) | `GET /common/currencies` | [docs](https://docs.oxapay.com/api-reference/common/supported-currencies2) |
| [List Supported Fiat Currencies](actions/list-supported-fiat-currencies.md) | `GET /common/fiats` | [docs](https://docs.oxapay.com/api-reference/common/supported-fiat-currencies2) |
| [List Supported Networks](actions/list-supported-networks.md) | `GET /common/networks` | [docs](https://docs.oxapay.com/api-reference/common/supported-networks) |
| [Revoke Static Address](actions/revoke-static-address.md) | `POST /payment/static-address/revoke` | [docs](https://docs.oxapay.com/api-reference/payment/revoking-static-address) |
