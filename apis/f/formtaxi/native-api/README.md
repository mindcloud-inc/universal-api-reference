# Form.taxi: Native API Reference

A consolidated summary of Form.taxi's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.form.taxi/en/api
- **OpenAPI specification:** https://docs.form.taxi/APIs/Form/openapi.yaml
- **API base URL:** `https://form.taxi/api/v1`

## Authentication

### API Key

Connect with a form-specific Form.taxi API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.form.taxi/en/api-form-submissions#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Endpoint](actions/create-endpoint.md) | `POST /create-endpoint` | [docs](https://docs.form.taxi/en/api-create-endpoint) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /form/submissions/:formCode` | [docs](https://docs.form.taxi/en/api-form-submissions) |
