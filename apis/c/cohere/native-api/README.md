# Cohere: Native API Reference

A consolidated summary of Cohere's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.cohere.com/reference/about
- **API base URL:** `https://api.cohere.com`

## Authentication

### API Key

Use a Cohere API key. Cohere authenticates requests with Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cohere.com/v1/reference/about)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `next_page_token`.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Embed Job](actions/cancel-embed-job.md) | `POST /v1/embed-jobs/:id/cancel` | [docs](https://docs.cohere.com/reference/cancel-embed-job) |
| [Chat](actions/chat.md) | `POST /v1/chat` | [docs](https://docs.cohere.com/reference/chat-v1) |
| [Create Embed Job](actions/create-embed-job.md) | `POST /v1/embed-jobs` | [docs](https://docs.cohere.com/reference/create-embed-job) |
| [Delete Dataset](actions/delete-dataset.md) | `DELETE /v1/datasets/:datasetId` | [docs](https://docs.cohere.com/reference/delete-dataset) |
| [Detokenize](actions/detokenize.md) | `POST /v1/detokenize` | [docs](https://docs.cohere.com/v1/reference/detokenize) |
| [Embed](actions/embed.md) | `POST /v1/embed` | [docs](https://docs.cohere.com/v1/reference/embed) |
| [Get Batch](actions/get-batch.md) | `GET /v2/batches/:id` | [docs](https://docs.cohere.com/reference/get-batch) |
| [Get Dataset](actions/get-dataset.md) | `GET /v1/datasets/:datasetId` | [docs](https://docs.cohere.com/reference/get-dataset) |
| [Get Dataset Usage](actions/get-dataset-usage.md) | `GET /v1/datasets/usage` | [docs](https://docs.cohere.com/reference/get-dataset-usage) |
| [Get Embed Job](actions/get-embed-job.md) | `GET /v1/embed-jobs/:id` | [docs](https://docs.cohere.com/reference/get-embed-job) |
| [List Batches](actions/list-batches.md) | `GET /v2/batches` | [docs](https://docs.cohere.com/reference/list-batches) |
| [List Datasets](actions/list-datasets.md) | `GET /v1/datasets` | [docs](https://docs.cohere.com/reference/list-datasets) |
| [List Embed Jobs](actions/list-embed-jobs.md) | `GET /v1/embed-jobs` | [docs](https://docs.cohere.com/reference/list-embed-jobs) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://docs.cohere.com/reference/list-models) |
| [Rerank](actions/rerank.md) | `POST /v1/rerank` | [docs](https://docs.cohere.com/v1/reference/rerank) |
| [Tokenize](actions/tokenize.md) | `POST /v1/tokenize` | [docs](https://docs.cohere.com/v1/reference/tokenize) |
