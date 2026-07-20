# Swiss QR Invoice: Native API Reference

A consolidated summary of Swiss QR Invoice's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://magicheidi.ch/qr-invoice-developer-api
- **API base URL:** `https://europe-west6-magic-heidi.cloudfunctions.net`

## Authentication

### API Key Query

Custom auth for Swiss QR Invoice. Stores the provider API key and passes it via the `key` query parameter.

### Credentials

- **API Key:** `apiKey` · optional · Swiss QR Invoice API key passed via the `key` query parameter.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `input.result`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Minimal Invoice](actions/generate-minimal-invoice.md) | `POST /create_invoice_abstract_v1d` | [docs](https://github.com/magic-heidi/swiss-invoice-qr-code-api#generate-a-minimal-invoice) |
