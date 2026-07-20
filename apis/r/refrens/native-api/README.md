# Refrens: Native API Reference

A consolidated summary of Refrens's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.refrens.com/api/docs/
- **API base URL:** `https://api.refrens.com`

## Authentication

### JWT Bearer Token

Refrens custom JWT bearer authentication. Refrens documents creating a token with appId and appSecret, or self-signing a token with the private key provided by Refrens.

### Credentials

- **Access Token:** `accessToken` · required · JWT bearer token used in the Authorization header for protected Refrens API calls.
- **Business URL Key:** `urlKey` · required · Refrens business urlKey used in business-scoped endpoint paths.
- **App ID:** `appId` · optional · Refrens appId used by the token creation endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://www.refrens.com/api/docs/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `$limit` in the query string to set the page size (default 100; accepted range 1–100). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Invoice Payment](actions/add-invoice-payment.md) | `POST /businesses/:urlKey/invoices/:invoice/payments` | [docs](https://www.refrens.com/api/docs/payment-updates/) |
| [Cancel Invoice](actions/cancel-invoice.md) | `PATCH /businesses/:urlKey/invoices/:invoice` | [docs](https://www.refrens.com/api/docs/invoices/) |
| [Create Business](actions/create-business.md) | `POST /businesses` | [docs](https://www.refrens.com/api/docs/business/) |
| [Create Expenditure](actions/create-expenditure.md) | `POST /businesses/:urlKey/expenditures` | [docs](https://www.refrens.com/api/docs/expenditure/) |
| [Create Invoice](actions/create-invoice.md) | `POST /businesses/:urlKey/invoices` | [docs](https://www.refrens.com/api/docs/invoices/) |
| [Create Token](actions/create-token.md) | `POST /authentication` | [docs](https://www.refrens.com/api/docs/authentication/) |
| [Generate Invoice IRN](actions/generate-invoice-irn.md) | `POST /businesses/:urlKey/invoices/:invoice/irn` | [docs](https://www.refrens.com/api/docs/generate-einvoice/) |
| [Get Invoice](actions/get-invoice.md) | `GET /businesses/:urlKey/invoices/:invoiceId` | [docs](https://www.refrens.com/api/docs/invoices/) |
| [List Invoice Payments](actions/list-invoice-payments.md) | `GET /businesses/:urlKey/invoices/:invoice/payments` | [docs](https://www.refrens.com/api/docs/payment-updates/) |
| [List Invoices](actions/list-invoices.md) | `GET /businesses/:urlKey/invoices` | [docs](https://www.refrens.com/api/docs/invoices/) |
| [Send Invoice Email](actions/send-invoice-email.md) | `POST /businesses/:urlKey/invoices/:invoiceID/email` | [docs](https://help.refrens.com/en/article/how-to-trigger-emails-for-all-your-documents-via-api-1khpmic/) |
| [Validate Token](actions/validate-token.md) | `POST /authentication` | [docs](https://www.refrens.com/api/docs/authentication/) |
