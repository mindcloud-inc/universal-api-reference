# PDF4me Connect: Native API Reference

A consolidated summary of PDF4me Connect's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.pdf4me.com/pdf4me-api/getting-started/
- **API base URL:** `https://api.pdf4me.com`

## Authentication

### API Key

Paste the PDF4me API key from the API Portal or the PDF4me account settings page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.pdf4me.com/power-automate/authorization/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Validate Credentials](actions/validate-credentials.md) | `POST /api/v2/GetPdfMetadata` | [docs](https://docs.pdf4me.com/pdf4me-api/pdf/get-pdf-metadata/) |
