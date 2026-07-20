# Moorcheh: Native API Reference

A consolidated summary of Moorcheh's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.moorcheh.ai/api-reference/introduction
- **API base URL:** `https://api.moorcheh.ai/v1`

## Authentication

### API Key

Authenticate Moorcheh API requests with an API key in the x-api-key header.

### Credentials

- **Moorcheh API key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.moorcheh.ai/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Namespace](actions/create-namespace.md) | `POST /namespaces` | [docs](https://docs.moorcheh.ai/api-reference/namespaces/create) |
| [Delete Documents](actions/delete-documents.md) | `POST /namespaces/:namespace_name/documents/delete` | [docs](https://docs.moorcheh.ai/api-reference/data/delete) |
| [Delete File](actions/delete-file.md) | `DELETE /namespaces/:namespace_name/delete-file` | [docs](https://docs.moorcheh.ai/api-reference/data/delete-file) |
| [Delete Namespace](actions/delete-namespace.md) | `DELETE /namespaces/:namespace_name` | [docs](https://docs.moorcheh.ai/api-reference/namespaces/delete) |
| [Delete Vectors](actions/delete-vectors.md) | `POST /namespaces/:namespace_name/vectors/delete` | [docs](https://docs.moorcheh.ai/api-reference/data/delete) |
| [Fetch Text Data](actions/fetch-text-data.md) | `GET /namespaces/:namespace_name/documents/fetch-text-data` | [docs](https://docs.moorcheh.ai/api-reference/data/fetch-text-data) |
| [Generate AI Answer](actions/generate-ai-answer.md) | `POST /answer` | [docs](https://docs.moorcheh.ai/api-reference/ai/generate) |
| [Get Documents](actions/get-documents.md) | `POST /namespaces/:namespace_name/documents/get` | [docs](https://docs.moorcheh.ai/api-reference/data/get-documents) |
| [Get Upload File URL](actions/get-upload-file-url.md) | `POST /namespaces/:namespace_name/upload-url` | [docs](https://docs.moorcheh.ai/api-reference/data/upload-file-url) |
| [List Namespaces](actions/list-namespaces.md) | `GET /namespaces` | [docs](https://docs.moorcheh.ai/api-reference/namespaces/list) |
| [Search](actions/search.md) | `POST /search` | [docs](https://docs.moorcheh.ai/api-reference/search/query) |
| [Upload Text Data](actions/upload-text-data.md) | `POST /namespaces/:namespace_name/documents` | [docs](https://docs.moorcheh.ai/api-reference/data/upload-text) |
| [Upload Vector Data](actions/upload-vector-data.md) | `POST /namespaces/:namespace_name/vectors` | [docs](https://docs.moorcheh.ai/api-reference/data/upload-vector) |
