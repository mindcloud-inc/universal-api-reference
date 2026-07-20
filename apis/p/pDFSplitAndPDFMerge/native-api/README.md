# PDF Split and PDF Merge: Native API Reference

A consolidated summary of PDF Split and PDF Merge's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://pdfapihub.com/docs
- **API base URL:** `https://pdfapihub.com/api/v1`

## Authentication

### API Key

Connect with your PDF API Hub API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
CLIENT-API-KEY: <apiKey>
```

[Official authentication documentation](https://pdfapihub.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500).

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Files](actions/list-files.md) | `GET /file/list` | [docs](https://pdfapihub.com/list-files) |
