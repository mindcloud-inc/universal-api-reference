# httpSMS: Native API Reference

A consolidated summary of httpSMS's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.httpsms.com/index.html
- **OpenAPI specification:** https://api.httpsms.com/doc.json
- **API base URL:** `https://api.httpsms.com/v1`

## Authentication

### API Key

Use your httpSMS account API key from Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.httpsms.com/introduction/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–20). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://api.httpsms.com/index.html#/Messages/get_messages) |
