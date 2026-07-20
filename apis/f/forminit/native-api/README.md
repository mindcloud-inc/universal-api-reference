# Forminit: Native API Reference

A consolidated summary of Forminit's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://forminit.com/docs/
- **API base URL:** `https://api.forminit.com`

## Authentication

### X-API-Key

API key for protected forms and higher rate limits.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://forminit.com/docs/submit-form-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 30). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Submissions](actions/list-submissions.md) | `GET /v1/forms/:formId` | [docs](https://forminit.com/docs/list-submissions-api/) |
| [Submit Form](actions/submit-form.md) | `POST /f/:formId` | [docs](https://forminit.com/docs/submit-form-api/) |
