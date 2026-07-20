# Graphor: Native API Reference

A consolidated summary of Graphor's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.graphorlm.com/
- **API base URL:** `https://sources.graphorlm.com`

## Authentication

### API Key

Use a Graphor project API token to access the public Sources, Chat, and Extraction APIs.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.graphorlm.com/guides/api-tokens)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask Documents](actions/ask-documents.md) | `POST /ask-sources` | [docs](https://docs.graphorlm.com/api-reference/chat-api) |
| [Ask Documents With Structured Output](actions/ask-documents-with-structured-output.md) | `POST /ask-sources` | [docs](https://docs.graphorlm.com/api-reference/chat-api) |
| [Continue Document Conversation](actions/continue-document-conversation.md) | `POST /ask-sources` | [docs](https://docs.graphorlm.com/api-reference/chat-api) |
| [Crawl URL Sources](actions/crawl-url-sources.md) | `POST /ingest-url` | [docs](https://docs.graphorlm.com/api-reference/sources/upload#ingest-url) |
| [Delete Source](actions/delete-source.md) | `DELETE /delete` | [docs](https://docs.graphorlm.com/api-reference/sources/delete) |
| [Extract Structured Data](actions/extract-structured-data.md) | `POST /run-extraction` | [docs](https://docs.graphorlm.com/api-reference/extract-api) |
| [Extract Structured Data By File Name](actions/extract-structured-data-by-file-name.md) | `POST /run-extraction` | [docs](https://docs.graphorlm.com/api-reference/extract-api) |
| [Get Build Status](actions/get-build-status.md) | `GET /builds/{buildId}` | [docs](https://docs.graphorlm.com/api-reference/sources/upload) |
| [Get Build Status With Elements](actions/get-build-status-with-elements.md) | `GET /builds/{buildId}` | [docs](https://docs.graphorlm.com/api-reference/sources/upload#get-build-status) |
| [Get Source Elements](actions/get-source-elements.md) | `GET /get-elements` | [docs](https://docs.graphorlm.com/api-reference/sources/list-elements) |
| [Get Source Elements By Type](actions/get-source-elements-by-type.md) | `GET /get-elements` | [docs](https://docs.graphorlm.com/api-reference/sources/list-elements) |
| [Ingest File](actions/ingest-file.md) | `POST /ingest-file` | [docs](https://docs.graphorlm.com/api-reference/sources/upload) |
| [Ingest GitHub Repository](actions/ingest-github-repository.md) | `POST /ingest-github` | [docs](https://docs.graphorlm.com/api-reference/sources/upload#ingest-github) |
| [Ingest URL](actions/ingest-url.md) | `POST /ingest-url` | [docs](https://docs.graphorlm.com/api-reference/sources/upload#ingest-url) |
| [Ingest YouTube Video](actions/ingest-youtube-video.md) | `POST /ingest-youtube` | [docs](https://docs.graphorlm.com/api-reference/sources/upload#ingest-youtube) |
| [List Sources](actions/list-sources.md) | `GET /` | [docs](https://docs.graphorlm.com/api-reference/overview) |
| [List Sources By File ID](actions/list-sources-by-file-id.md) | `GET /` | [docs](https://docs.graphorlm.com/api-reference/sources/list) |
| [Reprocess Source](actions/reprocess-source.md) | `POST /reprocess` | [docs](https://docs.graphorlm.com/api-reference/sources/process) |
| [Retrieve Relevant Chunks](actions/retrieve-relevant-chunks.md) | `POST /prebuilt-rag` | [docs](https://docs.graphorlm.com/api-reference/prebuilt-rag-api) |
| [Retrieve Relevant Chunks By File Name](actions/retrieve-relevant-chunks-by-file-name.md) | `POST /prebuilt-rag` | [docs](https://docs.graphorlm.com/api-reference/prebuilt-rag-api) |
