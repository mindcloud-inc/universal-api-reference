# Langbase: Native API Reference

A consolidated summary of Langbase's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://langbase.com/docs/api-reference
- **OpenAPI specification:** https://api.langbase.com/openapi.json
- **API base URL:** `https://api.langbase.com`

## Authentication

### API Key

Use a Langbase User or Org API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://langbase.com/docs/api-reference/api-keys)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chunk Content](actions/chunk-content.md) | `POST v1/chunker` | [docs](https://langbase.com/docs/api-reference/chunker) |
| [Crawl Web Pages](actions/crawl-web-pages.md) | `POST v1/tools/crawl` | [docs](https://langbase.com/docs/api-reference/tools/crawl) |
| [Create Memory](actions/create-memory.md) | `POST v1/memory` | [docs](https://langbase.com/docs/api-reference/memory/create) |
| [Create Memory Document Upload URL](actions/create-memory-document-upload-url.md) | `POST v1/memory/documents` | [docs](https://langbase.com/docs/api-reference/memory/document-upload) |
| [Create Pipe](actions/create-pipe.md) | `POST v1/pipes` | [docs](https://langbase.com/docs/api-reference/pipe/create) |
| [Create Thread](actions/create-thread.md) | `POST v1/threads` | [docs](https://langbase.com/docs/api-reference/threads/create) |
| [Create Thread Messages](actions/create-thread-messages.md) | `POST v1/threads/:threadId/messages` | [docs](https://langbase.com/docs/api-reference/threads/append-messages) |
| [Delete Memory](actions/delete-memory.md) | `DELETE v1/memory/:memoryName` | [docs](https://langbase.com/docs/api-reference/memory/delete) |
| [Delete Memory Document](actions/delete-memory-document.md) | `DELETE v1/memory/:memoryName/documents/:documentName` | [docs](https://langbase.com/docs/api-reference/memory/document-delete) |
| [Delete Thread](actions/delete-thread.md) | `DELETE v1/threads/:threadId` | [docs](https://langbase.com/docs/api-reference/threads/delete) |
| [Delete Thread Message](actions/delete-thread-message.md) | `DELETE v1/threads/:threadId/messages/:messageId` | [docs](https://langbase.com/docs/api-reference/threads) |
| [Generate Embeddings](actions/generate-embeddings.md) | `POST v1/embed` | [docs](https://langbase.com/docs/api-reference/embed) |
| [Generate Images](actions/generate-images.md) | `POST v1/images` | [docs](https://langbase.com/docs/api-reference/images) |
| [Get Pipe](actions/get-pipe.md) | `GET v1/pipes/:ownerLogin/:pipeName` | [docs](https://langbase.com/docs/api-reference/pipe) |
| [Get Thread](actions/get-thread.md) | `GET v1/threads/:threadId` | [docs](https://langbase.com/docs/api-reference/threads/get) |
| [Get Trace](actions/get-trace.md) | `GET v1/traces/:traceId` | [docs](https://langbase.com/docs/api-reference) |
| [List Memories](actions/list-memories.md) | `GET v1/memory` | [docs](https://langbase.com/docs/api-reference/memory/list) |
| [List Memory Documents](actions/list-memory-documents.md) | `GET v1/memory/:memoryName/documents` | [docs](https://langbase.com/docs/api-reference/memory/document-list) |
| [List Models](actions/list-models.md) | `GET v1/models` | [docs](https://langbase.com/docs/api-reference) |
| [List Pipes](actions/list-pipes.md) | `GET v1/pipes` | [docs](https://langbase.com/docs/api-reference/pipe/list) |
| [List Thread Messages](actions/list-thread-messages.md) | `GET v1/threads/:threadId/messages` | [docs](https://langbase.com/docs/api-reference/threads/list-messages) |
| [List Traces](actions/list-traces.md) | `GET v1/traces` | [docs](https://langbase.com/docs/api-reference) |
| [Parse Document](actions/parse-document.md) | `POST v1/parser` | [docs](https://langbase.com/docs/api-reference/parser) |
| [Retrieve Memory Chunks](actions/retrieve-memory-chunks.md) | `POST v1/memory/retrieve` | [docs](https://langbase.com/docs/api-reference/memory/retrieve) |
| [Retry Memory Document Embeddings](actions/retry-memory-document-embeddings.md) | `GET v1/memory/:memoryName/documents/:documentName/embeddings/retry` | [docs](https://langbase.com/docs/api-reference/memory/document-embeddings-retry) |
| [Run Agent](actions/run-agent.md) | `POST v1/agent/run` | [docs](https://langbase.com/docs/api-reference/agent) |
| [Run Pipe](actions/run-pipe.md) | `POST v1/pipes/run` | [docs](https://langbase.com/docs/api-reference/pipe/run) |
| [Search Web](actions/search-web.md) | `POST v1/tools/web-search` | [docs](https://langbase.com/docs/api-reference/tools/web-search) |
| [Update Pipe](actions/update-pipe.md) | `POST v1/pipes/:pipeName` | [docs](https://langbase.com/docs/api-reference/pipe/update) |
| [Update Thread](actions/update-thread.md) | `POST v1/threads/:threadId` | [docs](https://langbase.com/docs/api-reference/threads/update) |
| [Update Thread Message](actions/update-thread-message.md) | `POST v1/threads/:threadId/messages/:messageId` | [docs](https://langbase.com/docs/api-reference/threads) |
