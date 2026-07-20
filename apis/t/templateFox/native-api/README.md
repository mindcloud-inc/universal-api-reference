# TemplateFox: Native API Reference

A consolidated summary of TemplateFox's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://templatefox.com/docs
- **OpenAPI specification:** https://api.templatefox.com/openapi.json
- **API base URL:** `https://api.templatefox.com`

## Authentication

### API Key

Connect to TemplateFox with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://templatefox.com/docs/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create PDF](actions/create-pdf.md) | `POST /v1/pdf/create` | [docs](https://templatefox.com/docs/api-reference) |
| [Create PDF Async](actions/create-pdf-async.md) | `POST /v1/pdf/create-async` | [docs](https://templatefox.com/docs/api-reference) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://templatefox.com/docs/api-reference) |
| [Get PDF Job](actions/get-pdf-job.md) | `GET /v1/pdf/jobs/{{job_id}}` | [docs](https://templatefox.com/docs/api-reference) |
| [Get Template Fields](actions/get-template-fields.md) | `GET /v1/templates/{{template_id}}/fields` | [docs](https://templatefox.com/docs/api-reference) |
| [List PDF Jobs](actions/list-pdf-jobs.md) | `GET /v1/pdf/jobs` | [docs](https://templatefox.com/docs/api-reference) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://templatefox.com/docs/api-reference) |
| [List Transactions](actions/list-transactions.md) | `GET /v1/account/transactions` | [docs](https://templatefox.com/docs/api-reference) |
