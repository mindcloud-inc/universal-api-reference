# aamarPay: Native API Reference

A consolidated summary of aamarPay's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://aamarpay.readme.io/reference/overview
- **API base URL:** `https://sandbox.aamarpay.com`

## Authentication

### Store ID + Signature Key

Use your aamarPay store ID and signature key.

### Credentials

- **Store ID:** `storeId` · required · Merchant ID provided by aamarPay.
- **Signature Key:** `signatureKey` · required · Signature key issued by aamarPay.

[Official authentication documentation](https://aamarpay.readme.io/reference/sandbox-credentials-1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Initiate Payment (Form Data)](actions/initiate-payment-form-data.md) | `POST /index.php` | [docs](https://aamarpay.readme.io/reference/initiate-payment-form-data) |
| [Initiate Payment (JSON)](actions/initiate-payment-json.md) | `POST /jsonpost.php` | [docs](https://aamarpay.readme.io/reference/initiate-payment-json) |
| [Search Transaction](actions/search-transaction.md) | `GET /api/v1/trxcheck/request.php` | [docs](https://aamarpay.readme.io/reference/search-transaction) |
