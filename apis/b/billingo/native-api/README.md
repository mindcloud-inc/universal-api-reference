# Billingo: Native API Reference

A consolidated summary of Billingo's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.billingo.hu/
- **OpenAPI specification:** https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15
- **API base URL:** `https://api.billingo.hu/v3`

## Authentication

### API Key

Authenticate Billingo API v3 requests with an API key in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developers.billingo.hu/)

## API conventions

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Tax Number](actions/check-tax-number.md) | `GET /utils/check-tax-number/:taxNumber` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Convert Legacy ID](actions/convert-legacy-id.md) | `GET /utils/convert-legacy-id/:id` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Copy Document](actions/copy-document.md) | `POST /documents/:id/copy` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Create Document Export](actions/create-document-export.md) | `POST /document-export` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Create Document From Proforma](actions/create-document-from-proforma.md) | `POST /documents/:id/create-from-proforma` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Download Document](actions/download-document.md) | `GET /documents/:id/download` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Download Document Export](actions/download-document-export.md) | `GET /document-export/:id/download` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Bank Account](actions/get-bank-account.md) | `GET /bank-accounts/:id` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Currency Conversion Rate](actions/get-currency-conversion-rate.md) | `GET /currencies` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Document By Vendor ID](actions/get-document-by-vendor-id.md) | `GET /documents/vendor/:vendorId` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Document Online Szamla Status](actions/get-document-online-szamla-status.md) | `GET /documents/:id/online-szamla` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Document Payments](actions/get-document-payments.md) | `GET /documents/:id/payments` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Document Public URL](actions/get-document-public-url.md) | `GET /documents/:id/public-url` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Organization](actions/get-organization.md) | `GET /organization` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Partner](actions/get-partner.md) | `GET /partners/:id` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Product Inventory Quantity](actions/get-product-inventory-quantity.md) | `GET /inventory/product/:id/quantity` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Server Time](actions/get-server-time.md) | `GET /utils/time` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Get Spending](actions/get-spending.md) | `GET /spendings/:id` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bank-accounts` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Document Blocks](actions/list-document-blocks.md) | `GET /document-blocks` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Document Reminders](actions/list-document-reminders.md) | `GET /documents/:id/reminders` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Partners](actions/list-partners.md) | `GET /partners` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [List Spendings](actions/list-spendings.md) | `GET /spendings` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Poll Document Export](actions/poll-document-export.md) | `GET /document-export/:id/poll` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Print POS Document](actions/print-pos-document.md) | `GET /documents/:id/print/pos` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
| [Send Document](actions/send-document.md) | `POST /documents/:id/send` | [docs](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15) |
