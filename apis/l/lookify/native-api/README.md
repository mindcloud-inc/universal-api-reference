# Lookify: Native API Reference

A consolidated summary of Lookify's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://lookify.io/assets/pdfs/enterprise_carrier_api_documentation.pdf
- **API base URL:** `https://lookify.io`

## Authentication

### API Key

Authenticate with the API key from the Lookify API Dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://lookify.io/dashboard/api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Lookup Carrier](actions/lookup-carrier.md) | `POST /api/enterprise/carrier` | [docs](https://lookify.io/assets/pdfs/enterprise_carrier_api_documentation.pdf) |
