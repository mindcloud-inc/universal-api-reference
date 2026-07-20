# AddressZen: Native API Reference

A consolidated summary of AddressZen's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.addresszen.com/
- **OpenAPI specification:** https://openapi.addresszen.com/openapi.json
- **API base URL:** `https://api.addresszen.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.addresszen.com/docs/guides/api-key.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Email Validation](actions/email-validation.md) | `GET /emails` | [docs](https://docs.addresszen.com/docs/api/api-reference.md) |
| [Phone Number Validation](actions/phone-number-validation.md) | `GET /phone_numbers` | [docs](https://docs.addresszen.com/docs/api/api-reference.md) |
