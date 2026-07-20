# Voyage: Native API Reference

A consolidated summary of Voyage's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.voyageai.com/reference
- **API base URL:** `https://api.voyageai.com`

## Authentication

### API Key

Authenticate with a Voyage AI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.voyageai.com/docs/api-key-and-installation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `last_id`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–10000). Use `after` in the query string as the pagination cursor.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | `POST /v1/batches/:batchId/cancel` | [docs](https://docs.voyageai.com/reference/cancel-batch) |
| [Create Batch](actions/create-batch.md) | `POST /v1/batches` | [docs](https://docs.voyageai.com/reference/create-batch) |
| [Generate Contextualized Embeddings](actions/generate-contextualized-embeddings.md) | `POST /v1/contextualizedembeddings` | [docs](https://docs.voyageai.com/reference/contextualized-embeddings-api) |
| [Generate Multimodal Embeddings](actions/generate-multimodal-embeddings.md) | `POST /v1/multimodalembeddings` | [docs](https://docs.voyageai.com/reference/multimodal-embeddings-api) |
| [Generate Text Embeddings](actions/generate-text-embeddings.md) | `POST /v1/embeddings` | [docs](https://docs.voyageai.com/reference/embeddings-api) |
| [List Batches](actions/list-batches.md) | `GET /v1/batches` | [docs](https://docs.voyageai.com/reference/list-batches) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://docs.voyageai.com/reference/list-files) |
| [Rerank Documents](actions/rerank-documents.md) | `POST /v1/rerank` | [docs](https://docs.voyageai.com/reference/reranker-api) |
| [Retrieve Batch](actions/retrieve-batch.md) | `GET /v1/batches/:batchId` | [docs](https://docs.voyageai.com/reference/retrieve-batch) |
| [Retrieve File](actions/retrieve-file.md) | `GET /v1/files/:fileId` | [docs](https://docs.voyageai.com/reference/retrieve-file) |
| [Retrieve File Content](actions/retrieve-file-content.md) | `GET /v1/files/:fileId/content` | [docs](https://docs.voyageai.com/reference/retrieve-file-content) |
| [Upload File](actions/upload-file.md) | `POST /v1/files` | [docs](https://docs.voyageai.com/reference/upload-file) |
