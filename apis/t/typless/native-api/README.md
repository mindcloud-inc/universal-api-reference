# Typless: Native API Reference

A consolidated summary of Typless's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://typless.gitbook.io/typlessapi/
- **OpenAPI specification:** https://typless.gitbook.io/typlessapi/api-docs/api-schema.md
- **API base URL:** `https://developers.typless.com`

## Authentication

### API Key

Use your Typless API key from Settings > Profile. Typless requires the exact header Authorization: Token <API_KEY>, so this app stores one API key secret and injects it through the shared API header.

[Official authentication documentation](https://typless.gitbook.io/typlessapi/authorization)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Document](actions/add-document.md) | `POST /api/v1/add-document` | [docs](https://typless.gitbook.io/typlessapi/methods/add-document) |
| [Add Document Async](actions/add-document-async.md) | `POST /api/v1/add-document-async` | [docs](https://typless.gitbook.io/typlessapi/methods/add-document-async) |
| [Add Document Feedback](actions/add-document-feedback.md) | `POST /api/v1/add-document-feedback` | [docs](https://typless.gitbook.io/typlessapi/methods/add-document-feedback) |
| [Extract Data](actions/extract-data.md) | `POST /api/v1/extract-data` | [docs](https://typless.gitbook.io/typlessapi/methods/extract-data) |
| [Extract Data Async](actions/extract-data-async.md) | `POST /api/v1/extract-data-async` | [docs](https://typless.gitbook.io/typlessapi/methods/extract-data-async) |
| [Extract Pretrained Model Data](actions/extract-pretrained-model-data.md) | `POST /api/v1/pretrained-models/[:model_name]` | [docs](https://typless.gitbook.io/typlessapi/methods/extract-data-with-pretrained-model) |
| [Get Extraction Data](actions/get-extraction-data.md) | `GET /api/v1/get-extraction-data` | [docs](https://typless.gitbook.io/typlessapi/typless/data-extraction/asynchronous-extraction) |
| [List Awaiting Poll Extractions](actions/list-awaiting-poll-extractions.md) | `GET /api/v1/awaiting-poll` | [docs](https://typless.gitbook.io/typlessapi/typless/data-extraction/asynchronous-extraction) |
| [Start Training](actions/start-training.md) | `POST /api/v1/start-training` | [docs](https://typless.gitbook.io/typlessapi/methods/start-training) |
