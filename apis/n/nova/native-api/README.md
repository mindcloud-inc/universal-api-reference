# Nova: Native API Reference

A consolidated summary of Nova's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://app.n0va.com/documentation
- **API base URL:** `https://app.n0va.com/v1/la`

## Authentication

### API Key

Authenticate Nova requests with a single API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · optional · Stored Nova API key used by the shared x-api-key request header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://app.n0va.com/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | `POST /rt/zapier/add/lead` | [docs](https://app.n0va.com/documentation) |
| [Get Authenticated Company](actions/get-authenticated-company.md) | `GET /admin/api/auth` | [docs](https://app.n0va.com/documentation) |
| [Get Live Lists](actions/get-live-lists.md) | `GET /admin/company/live-lists` | [docs](https://app.n0va.com/documentation) |
| [Update Lead](actions/update-lead.md) | `PUT /rt/update/lead` | [docs](https://app.n0va.com/documentation) |
